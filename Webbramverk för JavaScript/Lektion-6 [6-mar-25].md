**Vilka tre delar vill man ofta separera från varandra när man sätter upp struktur i en applikation? Varför gör man det?** 

De tre delar man vill separera är Presentation, vilket är den kod som handlar om vad som visas i ett användargränssnitt. I en React applikation är detta de html element som skapas.

Den andra delen är applikationslogik som styr hur applikationen beter sig och hanterar vissa situationer. 

Den tredje delen är den kod som styr hur data hanteras i en applikation. I en React applikation kan detta vara services som pratar med web api:er.

Detta för att det blir en tydligare struktur i applikationen. Lättare att förstå koden och lättare att hantera den. 

**Vad innebär att en komponent fungerar som en container? Hur fungerar ett Container/Presentation pattern?** 

Detta är ett pattern som används ibland i React. En container håller state, innehåller lifecycle events och logik. Den renderar inga html-element. Den skickar data till presentationskomponenterna.

En presentationskomponent har bara som uppgift att skapa html element som visas på webbisdan men innehåller inte något av det som en container gör. 

**Vad vill man uppnå med containers?** 

Man är ute efter “separation of concerns” dvs att få en tydlig struktur och att varje typ av av kod skall ligga på rätt ställe.

**Vilka olika strategier kan det finnas att arbeta med styling i React?**

Det går att använda inline-styling som innebär att all CSS skapas inne i komponenten genom styling objekt. Det flexibla mest sättet. Sedan går det att arbeta med vanliga externa CSS-filer. Men detta kan bli ett problem om man har många CSS-filer och samma namn på klasser i dessa. Då kan det bli namnkrockar. Ett sätt att komma runt detta är att arbeta med CSS moduler. Det går även att arbeta med ett externt CSS bibliotek, t.ex. Tailwind, Bootstrap eller Matrerial UI.

**De komponenter som en React lösning består av skall översättas till en webbsida. Man pratar om parent och child komponenter. Hur påverkar detta webbsidan som appen skapar?** 

Det komponentträd som skapas i React skall översättas till en webbsida. Där finns ett DOM träd som beskriver webbsidan. Den ordning som komponenterna ligger i React styr var i DOM trädet som komponentens element hamnar. Det betyder att det som en parent komponent renderar hamnar högre upp i DOM trädet än det som child komponenten renderar. 

---

**Routing** 

Routing innebär att man hanterar navigering mellan olika sidor i en Single Page Application. Istället för att ladda om hela sidan byter man ut delar av innehållet baserat på URL:en.

**BrowserRouter** 

En komponent från react-router-dom som använder webbläsarens vanliga historik-API (pushState, popState) för att hantera navigering. Den skapar en mer naturlig och SEO-vänlig routing med "vanliga" URL:er, t.ex. /home eller /about.

**HashRouter** 

En annan typ av router som använder en hash (\#) i URL:en för att hantera navigering, t.ex. www.example.com/\#/home. Den är bra om man bygger en app som inte har kontroll över serverkonfigurationen eftersom den alltid fungerar utan att behöva serverinställningar.

**NavLink**

En länk-komponent från react-router-dom som fungerar som \<Link\> med extra funktionalitet, t.ex. att lägga till en aktiv klass när länken är vald. Användbar för att markera vilken sida som är aktiv i en meny.