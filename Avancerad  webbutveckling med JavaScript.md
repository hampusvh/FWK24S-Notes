**Introduktion**

**Varför är säkerhet viktigt även i frontend?**

Frontend är den första kontaktpunkten mot användaren och all kod körs direkt i användarens webbläsare. Det gör den extra sårbar för attacker som:

- XSS (Cross-Site Scripting)  
- Dataintrång eller läckor  
- Otillåtna API-anrop

Vi hanterar ofta känslig användardata i frontend och därför är det viktigt att tänka på säkerhet \- det är inte bara backends ansvar.

**Vad kan hända utan skydd (t.ex. filtrering eller validering)?**

Om vi visar osanerad användarinmatning i t.ex. kommentarer, formulär eller chattmeddelanden kan angripare injicera skadlig kod som till exempel innebär att: 

- Cookies kan stjälas  
- Användaren kan omdirigeras till farliga sidor  
- Keyloggers kan installeras för att övervaka tangenttryckningar

**XSS**

Cross-Site Scripting (XSS) innebär att skadlig kod injiceras i webbsidan och körs i användarens webbläsare.

Tre vanliga typer:

- Stored: Den skadliga koden sparas i databasen (t.ex. via ett kommentarsfält).  
- Reflected: Koden skickas med i en URL eller formulär och speglas direkt tillbaka.  
- DOM-based: Frontendmanipulation direkt i DOM:en utan serverinblandning.

XSS uppstår ofta i öppna fält som:

- Formulär  
- Kommentarsfält  
- Sökfält  
- Chattfunktioner

Förutom att se snyggt ut handlar frontend också om:

- Tillgänglighet  
- Trygghet och korrekthet  
- Felhantering (t.ex. 404-sidor)  
- Validering direkt i HTML

