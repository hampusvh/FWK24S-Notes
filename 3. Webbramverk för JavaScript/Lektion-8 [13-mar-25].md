**Vad innebär prop drilling? Varför kan det vara ett problem?** 

I stora applikationer är det oftast ett stort komponentträd med många nivåer. Att skicka props data i flera led kallas för prop drilling. Detta kan leda till många omrendreringar vilket påverkar prestandan i applikationen. 

**Beskriv vad Context API är och hur det kan användas.** 

Funktionalitet i Reacts corebibliotek för att arbeta med global statehantering (för att undvika prop drilling). Används i större/medelstora lösningar. För de största enterprise lösningarna brukar ett externt statebibliotek användas, som till exempel Redux eller MobX. 

**Vad är en provider och vad är en consumer?** 

En provider sätts upp med createContext. Här samlas statedata och eventhandlers för att arbeta med statedata. En consumer är en komponent som kommunicerar med providern för att hämta data. 

**Nämn några skillnader mellan en container och en provider.** 

Mycket är gemensamt för dessa. I båda fallen samlas statehantering och eventhandlers i en komponent. Den stora skillnaden är att en container skickar data vidare som props, detta gör inte en provider. Det är enklare att styra åtkomsten för en provider genom att den läggs som en wrapper (skal)  kring antingen hela komponentträdet eller delar av det. 

**Vad är en hook i React och vilka typer kan hooks delas in i? Vad är en custom hook och när bör man skapa en sådan?** 

En hook är funktionalitet i Reacts corebibliotek som kan importeras och användas för funktionsbaserade komponenter. Övergripande typer kan vara performance, state, effect och ref hooks. Det finns totalt ca 15 inbyggda hooks och det går även att skapa egna custom hooks. Detta kan göras för att återanvända kod som används på många ställen i en applikation och en custom hook kan importeras till många komponenter.   
