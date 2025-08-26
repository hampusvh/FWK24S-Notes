**XSS (Cross-Site Scripting)**

XSS innebär att skadlig kod (ofta JavaScript) körs i användarens webbläsare istället för på servern.

Målet är att angriparen ska kunna:

- Stjäla användardata (t.ex. cookies eller inloggningar)  
- Lura användaren att skriva in känslig info  
- Dirigera användaren till falska webbplatser

Attacken sker ofta genom att användarinput (t.ex. ett felmeddelande, ett formulär eller ett sökfält) inte saneras ordentligt innan det visas på sidan.

När kan XSS uppstå?

- Dålig validering av inputfält  
- Användardata visas direkt utan att rensas  
- Innehåll från tredjepartsbibliotek   
- Avsaknad av säkerhetspolicys som CSP (Content Security Policy)

Är React säkert mot XSS?

React skyddar till viss del automatiskt. Det finns bibliotek man kan använda för att sanera HTML, exempelvis DOMPurify. 

Ett tips är också att använda innerText istället för innerHTML. 

**Protected Routes**

En protected route kräver att användaren är inloggad (autentiserad) för att komma åt en sida. Det fungerar som en “dörr med lås” i en React-applikation.  
Om användaren inte är inloggad skickas de vidare till exempelvis en inloggningssida (/sign-in).

Man använder protected routes för att skydda känsliga sidor som:

- Dashboard  
- Användarprofil  
- Inställningar

Det förbättrar säkerhet och integritet, särskilt när användaren har personliga data eller känsliga uppgifter på sidan.

För att implementera protected routes används React Router och skapar en komponent som kontrollerar inloggningen. Sedan “wrappar” man de sidor man vill skydda. Detta för att skyddade sidor ska få en gemensam layout. 

