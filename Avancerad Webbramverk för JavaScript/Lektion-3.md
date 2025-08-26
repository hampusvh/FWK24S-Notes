1. Vad är en XSS attack? Vilka 3 typer finns det & hur kan man motverka dem?

   Cross Site Scripting (XSS) \- Det är en attack mot säkerheten på klienten. Det kan även ske en form av injectionattack som sker i form av script, kod \= JavaScript. Det stöds av i princip varenda webbläsare som gör det tillgängligt, således också sårbart.

   3 typer:

   **Stored**: Attacken sker genom permanent lagrad data på servern, typ databas \- som sedan når ut till användare för “framtida besök”. Varje användare får ta del av scriptet/koden eller dylikt så är det potentiellt farligare då det når ut till mångfalden. 

   **Reflected**: Koden skickas till servern genom en request (via URL/formulär) och sedan reflekteras det tillbaka till klienten utan att de valideras. 

   **DOM-based**: Inträffar när en webbsida dynamiskt ändrar DOMen baserat på användarens input utan sanitering. 

   Motverkande åtgärder:

   \- DOMPurify (sanitering / validering)  
   \- CSP (Content Security Policy)  
   \- Escapa data (se ovan, men även textContent/innerText istället för innerHTML)  
   \- Kör över HTTPS (SSL, certifikat går att utfärda gratis på LetsEncrypt)  
   \- Använd React, eller annat MVVM (Model-View-ViewModel) ramverk, som har “inbyggda” säkerhetsåtgärder 

2. Vad är Protected Routes och hur fixar man det för React Router? Inkludera kodexempel. 

   Protected Routes innebär att man behöver vara behörig för att få åtkomst till en viss route / sida. 

3. Varför tjatar jag om att “inte lita på klienten”?   
     
   Klienten är exponerad för användaren, och kan manipuleras \- som att exempelvis injicera skadlig kod, ändra funktionalitet eller avlyssna kommunikation.   
     
   Användaren kan även ändra data och det finns en överhängande risk för att känslig data kan bli exponerad.   
     
   Därför, för att säkerställa att applikationen är säker och skyddad, bör säkerhetsrelaterade beslut göras på servern, och vi ska alltid validera och verifiera all data som skickas från klienten.   
     
     
     
   

**reCAPTCHA** 

CAPTCHA \= “Completely Automated Public Turing test to tell Computers and Humans Apart” 

reCAPTCHA \= Googles moderna CAPTCHA

Skyddar formulär från bottar, spam och missbruk

Vanlig i login-, register- och kontaktformulär

Varför? 

Botar utnyttjar formulär för att:

- Skicka spam  
- Skapa fejk-konton  
- Testa lösenord (credential stuffing)

CAPTCHA är ett första skyddslager innan datan skickas till servern

Användning i React:

Används ofta med biblioteket react-google-recaptcha, vilket gör det enkelt att integrera i formulär. Den returnerar en token som först skickas till servern för validering innan den skickas in.

**Nackdelar:**

- Svåra bildtester kan utesluta vissa användare (ex. synskadade).  
- Kan vara frustrerande, särskilt på mobil.  
- Google samlar data, vilket väcker frågor om integritet och GDPR.  
- Vissa avancerade botar kan ta sig förbi skyddet.

**Sammanfattning**

CAPTCHA är ett effektivt första försvar mot bottar, men bör kombineras med backend-validering och andra skydd. 

**dangerouslySetInnerHTML**

dangerouslySetInnerHTML är ett attribut i React som gör det möjligt att direkt rendera HTML-kod som sträng. Det används vid behov av dynamiskt HTML-innehåll – men innebär stora säkerhetsrisker.

**Risker**

- Säkerhet: Kan öppna för XSS-attacker om HTML-innehållet kommer från användare.  
- Tillgänglighet: Går runt Reacts interna säkerhetssystem och kan skapa hinder för användare med hjälpmedel.  
- Prestanda: Går runt Reacts virtuella DOM vilket kan ge långsammare rendering.  
- Kodunderhåll: Blandar HTML och JavaScript vilket gör koden svårare att läsa och underhålla.

**Alternativ**

- textContent eller innerText – visar text utan HTML-tolkning.  
- Skapa DOM-element manuellt via JavaScript.  
- Använd React-komponenter och skicka data via props (komponentkomposition).

**Säker användning med DOMPurify:**

Om man måste använda dangerouslySetInnerHTML, bör man först sanera HTML-innehållet med DOMPurify. Det tar bort farliga delar som \<script\>-taggar innan det renderas.

**Sammanfattning**

Undvik dangerouslySetInnerHTML om möjligt. Använd DOMPurify om det absolut behövs, för att minska risken för XSS-attacker.

**CSP (Content Security Policy)**

CSP är ett säkerhetsverktyg som hindrar att otillåten eller skadlig kod laddas in på din webbplats. Det används ofta som skydd mot XSS och liknande attacker.

**Hur det fungerar**

Man skriver en policy som bestämmer vilka domäner som får ladda skript, bilder, stilmallar med mera. Detta specificeras i direktiv som script-src, img-src, style-src osv.

**Varför är detta bra?**

Om någon försöker injicera skadlig kod på din sida (till exempel via ett formulär eller en länk) så kommer webbläsaren att blockera den direkt, eftersom den inte är tillåten enligt policyn.  
Detta gör CSP till en stark skyddsåtgärd, särskilt mot sårbarheter där angriparen försöker köra kod via webbsidan.

**Sammanfattning**

CSP är ett mycket effektivt sätt att höja säkerheten på en webbsida. Det stoppar skadlig kod från att laddas, ger full kontroll över innehållskällor och skyddar både dig och dina användare mot flera vanliga typer av attacker. Men det kräver lite eftertanke och testning för att fungera optimalt.

