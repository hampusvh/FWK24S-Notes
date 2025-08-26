**SRR** \- Server Side Rendering  
**CSR** \- Client Side Rendering

**SSR Servern läser (rendrerar) javascripten:** 

User Requests Page ➔  
Server Generates HTML ➔  
HTML Sent to Browser ➔  
Page is Displayed

**CSR Klienten läser (rendrerar) javascripten:**

User Requests Page ➔  
Server Sends Basic HTML & JavaScript ➔  
JavaScript Loads & Renders Content in Browser

**Node** gör att man kan köra Javascript på Server / Backend  
**NPM** (Node Package Manager) gör det möjligt för utvecklare att hantera, installera och dela paketerad kod

**MERN Stack ( MongoDB , Express , React , NodeJS )**

Express förenklar hanteringen av webbservrar i Node.js och ger en strukturerad och enkel metod för att bygga server logik

Importera:  
const express \= require('express')  
const path \= require(‘path’)

Köra:  
const app \= express()  
const PORT \= 3000

appget(‘/’ (req, res) \=\> {  
	res.json({message: ‘Hello World’})  
})

app.listen(PORT, () \=\> {  
	console.log(\`Listening in port: ${PORT}\`)  
})

**Localhost** \= "den här datorn" eller "min egen dator".

**localhost** \= **127.0.0.1**

**127.0.0.1:3000** : 

127.0.0.1: En standard-IP för localhost som alltid pekar tillbaka på den egna enheten.

:3000: Port 3000, där en viss tjänst, exempelvis en lokal server, kan köras.

**Socket**: Kombinationen 127.0.0.1:3000 skapar en socket

Json \= Ett sätt att spara data i en databas

Middleware används för att bearbeta data, logga information, autentisera användare, hantera fel, och mycket mer, innan själva begäran når sin slutpunkt.

