**Vad är state i React och hur fungerar det? Hur gör man om det finns flera värden som behöver hanteras?** 

En tanke i React är att en komponent skall kunna hålla sitt eget data. Detta kallas för state. Det hanteras av en hook som heter useState och genom state variabler. När state uppdateras renderas komponenten om.

**I JS finns nyckelorden async och await. Hur och när används dessa?** 

Dessa används vid asynkron programmering till exempel vid anrop till web api:er. Har man flera funktioner som anropar varandra måste alla dessa vara asynkrona. Detta görs genom att nyckelordet async sätts på funktionen. När man från en asynkron funktion anropar en annan funktion måste nyckelordet await användas framför anropet. 

**Det finns ett bibliotek som heter ReactDOM, vilken funktion har det i en React lösning?**

Det hanterar kopplingen mellan webbsidan och React appen. Hanterar den virtuella DOM:en. Används inte när man använder React Native.

**Vad är useEffect i React? Vad kan det användas till?** 

Det är en hook (funktionalitet i Reacts corebibliotek) som kan användas för att hantera lifecycle events. Detta är automatiserade händelser i en komponent som man kan fånga upp och koppla kod till. Detta kan t.ex. vara att man vill köra viss kod första gången en komponent laddas. 

**Vad är en service? Vilket är syftet med en service i en React lösning?**

Det är JS filer som innehåller funktioner som anropar web api:er. Dessa anrop skall inte ligga direkt i komponenterna utan i servicefiler. Detta ger en bättre struktur och det blir enklare att underhålla och testa applikationer.

Tre lager i en applikation

- Presentation  
- Logik  
- Data

Container & Presentational Components

Ett design pattern som ofta används för React komponenter. Syftet är att skilja på olika typer av komponenter med olika typ av funktion.

Delas upp i vanliga komponenter och container komponenter. 

Allt blir som ett träd av olika typer av komponenter.  
