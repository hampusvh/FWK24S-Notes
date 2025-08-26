# **Repetition**

1. **Vad är cookies? Vad är local- och sessionStorage? Hur används dessa? Ge kodexempel\!**   
     
   Cookies är små textfiler som sparar data i webbläsaren (men på faktiskt disk).  
   Det skickas med automatiskt i varje HTTP-req till servern. Vi kan använda det för att spara olika states, sessionhantering, autentisering (JWT), spårning, statistik mm.  
   Kan ha attribut som \`HttpOnly\`, \`Secure\`, \`SameSite\`.  
   localStorage och sessionStorage är nästan samma som cookies (att spara data i webbläsaren) men:  
- sessionStorage försvinner när man stänger tabb/webbläsare (inte laddar om sida)  
- localStorage försvinner när man raderar den programmatiskt eller slutanvändaren tar bort den manuellt.  
- datat är endast tillgängligt i JavaScript och skickas inte med i HTTP-requests (om du nu inte gör det själv i dina fetch anrop)

// Spara data  
localStorage.setItem('username', 'Anna');

// Spara objekt  
const person \= { name: 'Sebbe', age: 35, isTeacher: true }  
localStorage.setItem('person', JSON.stringify(person));

// Hämta data  
const user \= localStorage.getItem('username');  
console.log(user); // "Anna"  
const savedPerson \= JSON.parse(localStorage.getItem('person'));  
console.log(savedPerson) // ger oss objektet

// Ta bort data  
localStorage.removeItem('username');  
localStorage.removeItem('person');

// Rensa all data (domänoberoende)  
localStorage.clear();

2. **Vad är CORS och hur fungerar det? Ge kodexempel på servern\!**   
     
     
   Som standard så tillåts bara anrop från samma domän, och konceptet kallas för Cross Origin Resource Sharing (CORS). Det är dock vanligt att man kommunicerar cross-domain idag och då behöver vi applicera tillåtelse för detta.  
     
   Rent krasst på servern (node.js) så är det ett npm-paket som behöver installeras som heter cors (finns alternativ, men detta är vanligast):  
     
   npm i cors  
     
   const express \= require('express')  
   const cors \= require('cors')  
   const app \= express()  
     
   app.use(cors()) // här tillåter vi alla requests oavsett domän för alla endpoints vi kommer ha  
     
   const corsOptions \= {  
     origin: 'https://sebbe.netlify.app', // Tillåt endast denna domän  
     methods: \['GET', 'POST'\],      // Tillåtna metoder  
     allowedHeaders: \['Content-Type', 'Authorization'\], // Tillåtna headers  
   };  
     
   app.use(cors(corsOptions))  
     
   app.post('/data', endpointMiddleware, (req, res) \=\> {  
     res.json({ message: 'Hej från servern\!' });  
   });  
     
   const endpointMiddleware \= () \=\> {  
     // handle requests here, prevent body to be populated etc  
   })  
     
     
     
     
     
     
     
3. **Vad är syftet med Context API i React och när är det lämpligt att använda det? Vad är dem 3 huvuddelarna & deras roll?** 

   Context APIet används för att hantera globala states och för att undvika "prop-drilling" (data som skickas genom flera komponenter i nivåer nedåt, "pass on" även om endast en komponent tar del av datan/funktionen)

   

   De 3 huvuddelarna i Context API:

   

   React.createContext() som skapar kontext som kan delas mellan komponenter

   

        import { createContext } from 'react'

        const UserContext \= createContext()

   

   Provider (tillhandahåller värdet) och gör state/data tillgängligt för våra child komponenter

   

        \<UserContext.Provider value={{ user, setUser }}\>

          {children}

        \</UserContext.Provider\>

   

   Consumer (hämtar värdet) och får tillgång till kontextet, används med useContext hooken

   

         const { user } \= useContext(UserContext);

   

   \- \- \- \- \- \- \- \- \- \- \- \- \- \- \- \- \- \- \- \- \- \- \- \- \- \- \- \- 

   

   📌 Exempel på Context API i praktiken (användarhantering)  

   

   import React, { createContext, useContext, useState } from "react";

   

   // 1\. Skapa Context

   export const UserContext \= createContext();

   

   // 2\. Skapa Provider

   export const UserProvider \= ({ children }) \=\> {

     const \[user, setUser\] \= useState(null);

     return (

       \<UserContext.Provider value={{ user, setUser }}\>

         {children}

       \</UserContext.Provider\>

     );

   };

   

   // 3\. Skapa en hook för att använda kontexten

   export const useUser \= () \=\> useContext(UserContext);

   

   // 4\. Använd kontext i en komponent

   const Profile \= () \=\> {

     const { user } \= useUser();

     return \<h2\>Inloggad som: {user ? user.name : "Gäst"}\</h2\>;

   };

   

   

   // 5\. Använd Provider i App.js

   import UserProvider from '../context/UserProvider'

   

   export default function App() {

     return (

       \<UserProvider\>

         \<Profile /\>

       \</UserProvider\>

     );

   }

---

# **JWT och Säkerhet**

**Säkerhet i SPA (Single Page Applications)**

En SPA fungerar ungefär som andra webbapplikationer men kräver också säkerhetsåtgärder för att hantera inloggningar och användare. Vanligtvis använder man cookies och HTTPS för att skydda kommunikationen. Eftersom SPA:er ofta kommunicerar med API:er behövs det en bra metod för verifiering, och då är JWT en vanlig lösning.

**JWT (JSON Web Token)**

JWT är en standard för autentisering som kom 2010\. Den är mycket vanlig idag, särskilt för att skydda API:er. Till exempel används JWT i många av Googles API:er. Det fungerar i flera olika miljöer, bland annat JavaScript och .NET.  
JWT används för att skapa så kallade access tokens. En access token är en nyckel som visar att användaren är autentiserad. Informationen i en JWT är ett krypterat JSON-objekt och måste alltid skickas över en säker anslutning (HTTPS).

**Hur fungerar JWT?**

1. Generering: Servern skapar en token som bekräftar användarens identitet.  
2. Utskicken: Denna token skickas till klienten (t.ex. en webbläsare).  
3. Användning: Klienten skickar tillbaka token vid varje förfrågan till servern.  
4. Verifiering: Servern kontrollerar att token är giltig innan den skickar data tillbaka.

JWT är ett exempel på "stateless authentication". Det betyder att information om inloggning inte sparas på servern som vid sessions, utan klienten ansvarar för att skicka med sin token.

**Var lagrar man JWT?**

Det bästa och säkraste sättet är att lagra token i en HttpOnly-cookie. En HttpOnly-cookie är inte tillgänglig via JavaScript, vilket skyddar den mot XSS-attacker. Den skickas automatiskt tillbaka till servern med varje förfrågan.

Att lagra JWT i localStorage eller sessionStorage är möjligt men mindre säkert eftersom de kan läsas av skadlig kod vid XSS.

**JWT i praktiken**

- JWT innehåller information om användaren i krypterad form.  
- Man kan sätta ett utgångsdatum för hur länge en token gäller.  
- Token skickas med i en HTTP-förfrågan, vanligtvis i fältet Authorization.

