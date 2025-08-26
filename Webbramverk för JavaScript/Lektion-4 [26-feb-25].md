### **Synkron & Asynkron Programmering** 

Synkron programmering betyder att koden körs rad för rad, i ordning. Varje steg måste bli klart innan nästa kan köras. Om en rad tar lång tid att köra, till exempel att hämta data från en server, måste resten av programmet vänta tills det är klart.

Asynkron programmering löser detta genom att vissa operationer kan påbörjas och sedan körs resten av koden utan att behöva vänta. När den asynkrona uppgiften är färdig, kan den skicka tillbaka resultatet och fortsätta därifrån. Exempel på tekniker för asynkron programmering är callbacks, promises och async/await.

### **Callback** 

En callback är en funktion som skickas som ett argument till en annan funktion och körs senare när den behövs. Det är ett sätt att hantera asynkrona uppgifter, där man kan säga: "När den här uppgiften är klar, kör denna funktion".

Problemet med callbacks är att om man behöver göra flera saker i rad, kan man få något som kallas “callback hell” eller “pryamid of doom”, där koden blir svår att läsa och förstå.

### **setTimeout**  setTimeout är en funktion i JavaScript som gör att en annan funktion körs efter en viss tid. Den tar två argument: en funktion att köra, och tiden i millisekunder  (1000 ms \= 1 sekund).

### 

### **Anonym funktion** 

En anonym funktion är en funktion utan namn. Den används ofta när vi bara behöver funktionen vid ett specifikt tillfälle, till exempel som en callback-funktion.

Anonyma funktioner används ofta i event listeners, callbacks och andra platser där vi inte behöver återanvända funktionen senare.

