**Vad är routing och hur fungerar det?**

Routing handlar om att mappa en url med en funktion eller komponent för att styra ett anrop. Kan ske på frontendsidan genom att man navigerar mellan olika komponenter. Kan ske på backendsidan i ett web api genom att url:en kopplas till en endpoint. 

**Beskriv vad react-router är?** 

Ett externt bibliotek för routing. Laddas ned som ett npm-paket. Routing är inte inbyggt i react till skillnad från t.ex. Angular och Vue. Då måste det användas ett externt bibliotek för detta. Den absolut vanligaste lösningen är att använda React-router för detta. 

**Beskriv hur react-router kan användas i en React lösning.**

Det går att sätta upp en navigeringsmeny med Navlink och Routes. Då navigerar man i applikationen med hjälp av url:en. Det går även att koppla navigering till knappar och andra html element. 

**Varför brukar man skilja på pages och components i en React lösning?** 

En page är en mer övergripande komponent som man kopplar en Route till (dvs navigerar till). Den består i sin tur av komponenter som är mindre delar av sidan (byggstenar). 

**Vad är routing parametrar och hur kan dessa användas för att göra komponenter mer flexibla?** 

Det är värden som skickas med via routen i url:en. Fungerar som props men skickas in via routen istället. Brukar användas för att hämta det data som visas i komponenten. Detta gör komponenter mer flexibla. 

**React \- Context API** 

En applikation består av ett träd med komponenter som samverkar i olika nivåer. State data skickas som props ibland i flera steg innan det används (prop drilling). Men det här innebär att många komponenter rendreras om i onödan och detta leder till försämrad prestanda.

För att motverka detta samlar man state-hantering centralt, där många komponenter kan gå för att hämta sitt state-data.   
Det första man behöver göra är att sätta upp en Provider, som fungerar som den centrala datakällan. Det är en övergripande komponent med state. 

Sedan behövs en rootkomponent för att använda providern, och i sin tur kan alla komponenter i trädet komma åt den. 

En provider hanterar state data men detta är åtkomligt i alla komponenter utan att det behöver skickas som props. med useContext kan man “importera” state data. Detta är en global datakälla för hela applikationen. 

Redux & MoveX är två externa state-management bibliotek som ofta används i React. 