**State**

State kan man säga är som en “låda” där en komponent lagrar sin egen data. Den kan uppdatera lådan när något förändras, så att den senaste informationen visas. 

State gör komponenter dynamiska, varje komponent har sitt eget state och det påverkar endast den specifika komponenten.

För att använda state måste man importera useState.

Detta kallas för Hook, och useState är den vanligaste hooken i React. 

**Hook**

En Hook är en funktion i React som låter oss använda state och andra React-funktioner i funktionella komponenter

### **Funktionella komponenter** 

En funktionell komponent är en vanlig JavaScript-funktion som returnerar JSX (React’s sätt att skriva HTML).

### **Asynkrona Anrop** 

Asynkrona anrop i React betyder att data skickas eller hämtas utan att stoppa resten av koden. I React används asynkrona anrop för att hämta data från en server eller ett API utan att frysa hela sidan.

### För att använda asynkrona anrop, används 

- fetch()  
- useEffect() 

fetch() hämtar data från en server.  
useEffect() används för att köra anropet när sidan laddas.

