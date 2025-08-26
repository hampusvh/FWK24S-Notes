# **Repetition**

1. **Vad är Netlify för något och varför använder man det? Finns det några alternativ?**   
     
   Netlify är en molnplattform (snarare tjänst) som syftar bland annat till att få upp sin lokala kod till molnet (alltså publikt på nätet). Se det som en modern ersättare, med enkelhet, till vad webbhotell med FTP-överföring var back in the day.   
     
   Molnplattform \= Azure, AWS (Amazon Web Services) eller GCP (Google Cloud Platform)  
     
   Gäller Netlify backend också? Nej tyvärr, det är till för JAM-stack applikationer (JavaScript, API, Markup) som kan byggas, deployas och hostas där. Alternativ till Netlify: Vercel Heroku, GitHub pages.  
     
   För backend då? Eller kombo av båda? Vercel, Glitch, Railway eller någon av molnplattformarna ovan (de kostar dock pengar).  
     
2. **Vad är bcryptjs och hur fungerar det? Finns det några alternativ?** 

   Det är ett Javascript bibliotek för att hasha lösenord, för att motverka att en angripare ser lösenordet i klartext (vid givet tillfälle) utan det är då saltat.

   Det ska vara svårare. Du skriver vanliga lösenord \- det saltas. 

   

   Lösenord \+ salt \= hashat lösenord (skickas till servern). 

   

   Den blir då oåterställbar men den kan jämföras med ett lösenord (som du då måste kunna) för att “avkoda” den.

   

   Bcrypt fungerar i två steg: 

   

1. Saltning: En unik slumpmässig sträng läggs till lösenordet.   
2. Hashing: Lösenordet \+ salt körs genom en algoritm som gör det långsamt (för att förhindra brute-force attacker).

   Den stora fördelen är att hashen ser olika ut även om två användare har samma lösenord, tack vare salting.

   

   Alternativ till bcrypt(js):

- argon2  
- pbkdf2

3. **Vad är & hur fungerar React Router? Ta gärna med ett kodexempel på hur man sätter upp React Router.** 

   Det är ett externt bibliotek för routing. Laddas ned som ett npm-paket. Routing är inte inbyggt i react till skillnad från t.ex. Angular och Vue. Då måste det användas ett externt bibliotek för detta. Den absolut vanligaste lösningen är att använda React-router för detta. 

   

   Det går att sätta upp en navigeringsmeny med Navlink och Routes. Då navigerar man i applikationen med hjälp av url:en. Det går även att koppla navigering till knappar och andra html element. 

   

   Importera Router, Routes från react-router-dom, wrappa det i app.jsx (eller main.jsx)

---

# **Cookies och Web Storage**

När man bygger webbaserade applikationer uppstår ofta behovet av att spara information direkt i webbläsaren, exempelvis för att komma ihåg en användares sökning eller innehållet i en varukorg. Denna data sparas vanligtvis i JSON-format och det finns olika tekniker för att hantera detta, främst cookies och web storage.

---

# **Cookies**

Cookies är små textfiler som lagras på klientens dator, antingen tillfälligt i minnet eller permanent på disk. De kan innehålla värden som används av klienten och som automatiskt skickas tillbaka till servern vid varje request. Både servern och klienten (via JavaScript) kan skapa cookies.

Cookies kan anpassas med olika inställningar:

- Expires: Bestämmer hur länge cookien ska sparas (sparas på disk).  
- Secure: Gör att cookien endast skickas via HTTPS.  
- HttpOnly: Gör cookien otillgänglig för JavaScript, ökar säkerheten.  
- Domain: Anger vilket domännamn cookien är kopplad till.

I Sverige måste webbplatser sedan 2011 informera användare om att cookies används och få deras samtycke.

---

# **HTML5 Web Storage**

Web Storage är en funktion i HTML5 som gör det möjligt att spara data lokalt i webbläsaren, utan att skicka informationen till servern. Detta sker helt och hållet på klientsidan via JavaScript.

Fördelar jämfört med cookies:

- Web storage är säkrare eftersom datan inte skickas till servern.  
- Det går att lagra upp till 5 MB data (jämfört med cirka 4 KB för cookies).  
- Datan kan hanteras med två olika alternativ: sessionStorage och localStorage.

---

# **Session Storage**

Session storage sparar data tillfälligt under en och samma session. När användaren stänger webbläsaren raderas informationen. Detta passar bra för tillfälliga värden, som exempelvis en sökning.

---

# **Local Storage**

Local storage fungerar på liknande sätt som session storage, men informationen sparas även efter att webbläsaren stängts ned. Datan ligger kvar tills den raderas manuellt eller via kod.

---

# **CORS (Cross-Origin Resource Sharing)**

I moderna webbapplikationer är det vanligt att olika system kommunicerar över olika domäner. Detta kallas cross-origin requests, vilket innebär att en webbplats skickar ett anrop till en server som ligger på en annan domän än den egna. 

För att skydda användare från potentiella säkerhetshot, som exempelvis CSRF-attacker, finns det en inbyggd säkerhetsmekanism i webbläsare som kallas Same-Origin Policy. Denna policy innebär att endast anrop från samma domän tillåts som standard.

För att möjliggöra kommunikation mellan olika domäner i en kontrollerad och säker form används CORS (Cross-Origin Resource Sharing). CORS är en standard framtagen av W3C som gör det möjligt för en server att specificera vilka domäner som får skicka förfrågningar till den, samt vilka metoder (exempelvis GET eller POST) som är tillåtna.

När en förfrågan skickas från en annan domän bifogar webbläsaren en Origin-header med information om ursprunget. Servern granskar denna och, om begäran är tillåten enligt CORS-policyn, svarar den med en Access-Control-Allow-Origin-header. 

I vissa fall gör webbläsaren först en så kallad preflight request för att kontrollera om själva anropet är tillåtet innan det verkliga anropet görs.

För att konfigurera CORS i ett Node.js-baserat web API används ofta Express tillsammans med npm-paketet cors. 

