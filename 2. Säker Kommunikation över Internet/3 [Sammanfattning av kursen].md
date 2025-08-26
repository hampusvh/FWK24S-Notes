**HTTPS** 

* Är krypterad kommunikation   
* Använder assymetrisk kryptering  
* Säkerkommunikation  
* Kräver certifikat  
* Vid uppstart utbyter klient och server publika nycklar med hjälp av clientHello och serverHello

**Certifikat**

* Utges av CA  
* Är publik nyckel \+ domän som certifieras (https)  
* Förmedlar tillit  
* Localhost går inte att certifiera  
* Man kan med hjälp av openssl signera ett eget certifikat  
* När vi lägger ut en app på molnet \- får vi ofta använda molnets certifikat

**Hashning**

* Vi lagrar inte lösenord ens i krypterad form  
* Hasning är en irreversibel process vilket hindrar läckage och ökar integritet

**Saltning**

* Vi förlänger lösenord med Salt för att öka tiden det tar att använda “brute force” för att knäcka lösenordet

**Autentisering**

* Något vi kan  
* något vi äger  
* något vi är  
* multi factor är några av dessa samtidigt  
* man autentiseras i ett sammanhang (context)  
* När vi är autentiserade får vi ett TOKEN (JWT) som bevis

**Auktorisering** 

* Vad vi får göra i ett system  
* Om ett Token (JWT) går att öppna är det bevis på att man är auktoriserad  
* Man kan lägga in en payload i en JWT  
* Payload kan innehålla attributet “role” som ger finare kontroll över auktorisering

**XSS (Cross Site Scripting)** 

* Sanitera all input

**CSRF (Cross Site Request Forgery)**

* Skapa ett CSRF Token för att klient ska kunna bevisa att anropet kommer från egen applikation.  
* CSRF Token får inte lagras i session eller i cookies om JWT finns i cookies.