**Vad är skillnaden mellan JS bibliotek och ramverk? Vad är ett webbramverk och vad är fördelarna med att använda ett sådant?** 

Ett JS bibliotek är kod förpackad i ett paket som innehåller viss funktionalitet. Kan tex var språkhantering. Har ett avgränsat syfte. 

Ett ramverk är fler bibliotek tillsammans som skapar en plattform för att bygga applikationer. Ett webbramverk är en plattform för att skapa SPA dvs Single Page Applications.

**Beskriv vad React är? Vilka två varianter finns det? Vad innebär virtulell DOM, JSX och Babel?** 

React är ett bibliotek för att skapa SPA applikationer som tagits fram av Facebook. Måste kombineras med andra bibliotek när man bygger applikationer. Finns i två varianter. React (Web) och React Native (cross-platform mest mobil). 

Moderna webbapplikationer har ofta ett stort DOM träd dvs många element på sidan. Detta kan ge dåliga prestanda om man bygger en SPA applikation med mycket DOM manipulation. För att optimera detta har React en virtuell DOM som är ett mellanled.

React består av två paket React (core) och ReactDOM (hanterar den virtuella DOM:en). 

JSX är en extension till JS. Gör det möjligt att blanda HTML och JS kod. När koden körs måste den omvandlas så att webbläsaren kan hantera den. Detta görs med en transpiler som heter Babel. 

**Vad är en komponent i React och hur fungerar den?** 

React bygger upp gränssnittet av komponenter som är små återanvändbara byggstenar. En komponent hanterar sitt eget beteende och data. Webbsidan består av många komponenter som samverkar. 

**Vad innebär render funktionalitet i en komponent? Vad skall man tänka på när det finns flera element med?** 

Render funktionalitet innbebär att en komponent returnerar HTML kod som styr hur komponenten visas. När man returnerar flera element måste det finnas en yttre tag/container runt dessa. Man skall undvika att lägga in en tom div eftersom det ger onödigt stort DOM träd. Då kan man använda React Fragment istället. Den syntax ni bör använda för det är \<\> Här läggs innehållet \</\>

**Vad är props i React? Hur fungerar det? Vad är destructing?** 

Props är Reacts sätt att skicka data mellan komponenter. Fungerar som ett stort objekt som kan innehålla enskilda värden och även arrayer. För att förenkla koden kan man använda destructing som är ett sätt att i JS ta ut värden från ett objekt och lägga i variabler. Förenklar koden men behöver inte användas. 

---

**React events** 

- Fungerar väldigt likt ett vanligt event i html men det finns några skillnader

- En anledning är att vanliga events kopplas till elements som ligger under DOM:en. Eftersom React inte arbetar direkt mot DOM:en fungerar även detta annorlunda. 

- Så React **hanterar inte DOM event direkt utan använder sitt eget sätt att hantera detta som kallas för Synthetic events.** 