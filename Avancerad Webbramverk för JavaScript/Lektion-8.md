**Repetition**

**1\. Hur fungerar registrering- & inloggningsdelen för Chatify APIet? Berätta kortfattat om flödet.**

Man hämtar först en CSRF token. Detta görs genom en PATCH mot /csrf och man får tillbaka en sträng som representerar en GUID.

Därefter gör man ett POST anrop mot /auth/register. Man behöver skicka data i bodyn som innehåller användare, lösenord, email, avatar och CSRF-token

**2\. Vad är CORS för något, vad kan vi göra på klienten respektive servern för att hantera det?**

CORS (Cross-Origin Resource Sharing) är en regel där servern talar om för webbläsaren vilka andra domäner som får hämta data från den

**3\. Varför gör man tester på frontend? Vad är RTL för något? Hur kan ett test se ut (med kod)?**

Man testar frontend för att se till att det man byggt faktiskt funkar som det ska och för att undvika att nya ändringar råkar sabba något som redan fungerar. RTL (React Testing Library) är ett testverktyg för React som låter en testa komponenterna på samma sätt som en användare faktiskt använder sidan, istället för att bara kolla hur koden ser ut inuti.

**4\) Vad är skillnaden på cookies och local-/sessionStorage? Ta gärna med exempel.**

Cookies är små textfiler som lagras av webbläsaren och skickas automatiskt till servern vid varje request. De kan sättas av både servern och klienten och har inställningar som expires, secure och HttpOnly. Används ofta för sessionshantering.

Local storage och Session storage är en del av Web Storage API och lagrar data direkt i webbläsaren utan att skicka den till servern automatiskt. Local storage sparas tills den raderas manuellt eller via kod. Session storage finns bara kvar tills fliken eller webbläsaren stängs.

---

**GDPR (General Data Protection Regulation)**

GDPR är en EU-lag som styr hur personuppgifter får samlas in och användas. Den började gälla 25 maj 2018 och gäller för alla inom EU. Poängen med lagen är att ge människor mer kontroll över sin egen data och göra det enklare för företag att följa reglerna.

Grunden i GDPR är att personuppgifter alltid ska behandlas lagligt, rättvist och öppet. Man får bara samla in uppgifter för ett bestämt och tydligt syfte och inte använda dem till något annat än det som var tänkt från början. Dessutom ska man bara samla in den information som verkligen behövs.

En viktig del är samtycke. För att få hantera personuppgifter måste användaren aktivt säga ja, till exempel genom att klicka i en ruta. Det får inte vara förkryssat i förväg. Samtycket ska vara frivilligt, tydligt och informerat, och det ska vara enkelt att ta tillbaka det.

GDPR ger också användare rätt att få veta vilka uppgifter som finns sparade om dem och rätt att få dem raderade.

För cookies betyder det att man måste tala om vilka cookies som används och varför, och be om lov innan man sparar dem. Användaren ska även kunna ändra eller ta bort sitt godkännande senare.

Inom webbutveckling finns till exempel biblioteket **React Cookie Consent** som gör det enkelt att lägga till en cookie-banner i en React-app. Man installerar det med npm install react-cookie-consent och använder sedan **\<CookieConsent\>** \- komponenten för att visa meddelandet. Viktigt att tänka på är att bannern ska synas men inte vara i vägen för mycket.

