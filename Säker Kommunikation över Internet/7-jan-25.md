1. Något man kan	(Lösenord)

2. Något man har	(BankID) 

3. Något man är 	(Fingeravtryck)  
   

IP \- Identify Provider

---

**Hashing**

Hashing är en process där ett lösenord omvandlas till en "hash" (en unik, fast längd sträng) med hjälp av en matematisk algoritm.

Hashar är enkelriktade, vilket innebär att du inte kan återställa det ursprungliga lösenordet från hash-värdet.

**Salting** 

Salting innebär att man lägger till en unik och slumpmässig sträng (en "salt") till lösenordet innan det hashas.

Detta gör att två användare som har samma lösenord inte får samma hash-värde.

Salten sparas oftast tillsammans med hash-värdet i databasen för att kunna verifiera lösenord senare.

**JWT (JSON Web Token)** 

En JWT-token är en sträng som innehåller information som kan användas för att verifiera en användare eller ge tillgång till en resurs.

**bcrypt**

När ett lösenord ska lagras, använder bcrypt en speciell algoritm för att:

- Lägga till en salt till lösenordet.  
- Hasha lösenordet med salten flera gånger, vilket gör processen långsammare.  
- Resultatet är en hash som lagras i databasen istället för själva lösenordet.

