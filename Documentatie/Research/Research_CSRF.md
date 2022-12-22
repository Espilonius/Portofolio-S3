# CSRF onderzoek

# Reading guide
- [Wat is CSRF?](#wat-is-csrf)
- [Hoe kan een CSRF aanval worden weerstaan?](#hoe-kan-een-csrf-aanval-worden-weerstaan)
    - [Wat is een CSRF aanval?](#wat-is-een-csrf-aanval)
    - [CSRF aanval voorkomen.](#csrf-aanval-voorkomen)
- [Hoe kan je kwetsbaarheden vinden in code?](#hoe-kan-je-kwetsbaarheden-vinden-in-code)
- [CSRF aanval demo.](#csrf-aanval-demo)
- [Resources](#resources)

---
## **Wat is CSRF?**
CSRF staat voor Cross-Site Request Forgery, dit is een type kwetsbaarheid waarbij de aanvaller misbruik maakt van een actieve gebruikerssessie. Hiermee kan de aanvaller je acties laten uitvoeren zonder dat je er erg in hebt. Zoals bijvoorbeeld op een linkje klinken waarbij dan wachtwoorden worden doorgegeven.

## **Hoe kan een CSRF aanval worden Weerstaan**
Om een CSRF aanval te weerstaan is het belangrijk om eerst te weten hoe een CSRF aanval eruit ziet.
![CSRF_Aanval](https://user-images.githubusercontent.com/58418773/208425341-ec69a48c-e0a1-45fa-93e3-a22ea4d6711e.png)

### **Wat is een CSRF aanval?**
Een CSRF aanval bestaat uit twee stappen van bovenaf gezien, namelijk:
1. Het slachtoffer moet op een linkje klikken waarmee een 'schadelijke' pagina of script wordt geladen.
2. Als het slachtoffer op de pagina is moet deze nog zelfstandig het verzoek 'voltooien', dit kan bijvoorbeeld een nagemaakte inlogpagina zijn waarop moet worden ingelogd of een banktransactie waar het slachtoffer mee bezig was.

Tijdens CSRF zie je vaak twee methodes terug komen waarmee een aanvaller een aanvraag kan manipuleren; HTTP GET en HTTP POST, hiernaast zijn ook nog andere methodes te gebruiken zoals HTTP PUT of HTTP DELETE.

### **CSRF aanval voorkomen.**
Er zijn verschillende manieren om een aanval zoals CSRF te voorkomen:
- altijd veilige, unieke wachtwoorden gebruiken.
- Wachtwoorden of actieve sessies nooit automatisch onthouden.
- NoScript plugin gebruiken in je webbrowser.
- CSRF-token gebruiken, dit is als het ware een extra cookie waarbij een unieke token gegenereerd wordt. deze verloopt na enige tijd.
- implementeren van CAPTCHA aan de serverkant.

## **Hoe kan je kwetsbaarheden vinden in code?**
Om kwetsbaarheden te vinden in code moet je op zoek gaan naar unieke keys die gebonden zijn aan een gebruiker is het veilig in de ogen van een CSRF aanval. Als er geen unieke key gebonden is aan een user wordt dat gezien als kwetsbaar, dus hier kan een kwaadaardig request worden gestuurd naar de applicatie. Hiervoor is een Session ID niet genoeg voor, want de Session ID wordt weggegooid als de gebruiker op een kwaadaardige link drukt. Dit komt omdat de gebruiker al is gevalideert.

## **CSRF aanval demo**
Om CSRF te demonstreren maak ik gebruik van DVWA, een webapplicatie die met opzet kwetsbaar is. Ik zal hierbij gebruik maken van Kali Linux en Burp Suite.
**Security Level – Low**
Wanneer ik de kwetsbare pagina open zie ik het volgende formulier; 
![formulier voor een nieuw admin wachtwoord.](https://user-images.githubusercontent.com/58418773/208429666-489fbf5c-ea7e-4241-806a-2cb1877eb8a5.png)
Om te kijken hoe de pagina werkt stel ik een nieuw wachtwoord in, dit doe ik via de ingebouwde webbrowser van Burp Suite. 

Zodra ik het wachtwoord verander krijg ik vanuit Burp Suite te zien dat de pagina een HTTP-GET aanvraag doet naar de server, in dit geval is dat om een nieuw wachtwoord in te stellen.
![Code_SLL](https://user-images.githubusercontent.com/58418773/208431033-6e738600-b443-47e3-9b79-89964c730356.png)
>http://192.168.146.128/vulnerabilities/csrf/password_new=password123&password_conf=password123&Change=Change HTTP/1.1

De URL kunnen we aanpassen naar eigen hand, dit kun je doen door ‘password123’ te veranderen naar bijvoorbeeld ‘helloworld’.
>http://192.168.146.128/vulnerabilities/csrf/password_new=helloworld&password_conf=helloworld&Change=Change HTTP/1.1

Wanneer deze link bij een gebruiker terecht komt die is ingelogd op DVWA en deze opent zal het wachtwoord veranderen naar ‘helloworld’ zonder dat degene dit doorheeft. 

Een URL zoals deze zou je, om het makkelijk te maken, op een website kunnen plaatsen (bijvoorbeeld XSS) of via een phishing mailtje naar de gebruiker kunnen sturen. 

**Security Level – Medium**
Zoals ik in de vorige uitwerking vertelde is het ook mogelijk om zulke URL’s te gebruiken en te verwerken in bijvoorbeeld een website. Om security level medium aan te tonen zal ik hier gebruik van maken.

Ik herhaal de stappen die ik tijdens de vorige demonstratie heb gebruikt, wanneer ik het wil veranderen zie ik dit niet meer mogelijk is.

![Code_SLM_1](https://user-images.githubusercontent.com/58418773/208433093-a46ab38a-7595-4e02-bd3a-fdac1d9b4e2b.png)

Wanneer ik vervolgens de URL opnieuw wil uitvoeren en daarbij de waardes van het wachtwoord verander krijg ik de volgende foutmelding. 

![CSRF_NOTCORRECT_SLM](https://user-images.githubusercontent.com/58418773/208434938-fca0bdab-74cc-4bfc-9afb-f6279f556032.png)

Als ik nu kijk naar de HTTP request die door Burp Suite is opgevangen valt mij iets op.

![Code_SLM_2](https://user-images.githubusercontent.com/58418773/208435406-ec8fc38f-c4ce-4022-91f4-c82e5f23e616.png)

Op regel 6 is nu geen zogenaamde HTTP Referer header meer te vinden, dit is een HTTP header die ervoor zorgt dat de webpagina een vorige webpagina kan ‘herkennen’. Hierdoor kun je niet meer opeens naar een pagina springen maar moet er een herkenbaar startpunt zijn.

Het is helaas erg makkelijk om deze header na te bootsen, dit kan middels een simpele webpagina en Burp Suite. 

![Code_SLM_3](https://user-images.githubusercontent.com/58418773/208435653-c48aa78f-e828-4ba7-9381-200a3a52c161.png)

Vervolgens zorg ik ervoor dat ik de request opvang met Burp Suite, hierin kan ik namelijk veranderingen inbrengen.

![Code_SLM_4](https://user-images.githubusercontent.com/58418773/208435849-5906219c-f7db-4c26-adf3-a3e54112bca1.png)

Als ik nu de request doorstuur naar de webpagina zul je zien dat hij nu geaccepteerd word.

![Code_PWC](https://user-images.githubusercontent.com/58418773/208436096-a29b52f1-da4f-4201-96f1-aaf946a5edc8.png)

---
### **Resources**
- [Cross Site Request Forgery (CSRF)](https://owasp.org/www-community/attacks/csrf)
- [Kwetsbaarheden opsporen](https://owasp.org/www-project-code-review-guide/reviewing-code-for-csrf-issues)
- [Wat is CSRF?](https://www.remcoboon.nl/cross-site-request-forgery-csrf/)