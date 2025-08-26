**Vad är cURL?**

cURL är ett kommandoradsverktyg som används för att skicka och ta emot data över internet. Det är särskilt användbart för att kommunicera med webbservrar och API:er.

cURL används till att: 

- Hämta data från en webbsida  
- Skicka data till ett API (t.ex. skapa en användare eller logga in)  
- Testa om en server eller endpoint svarar som den ska

### Exempel på hur man kan använda cURL:

#### **1\. Hämta en webbsida:**

curl https://example.com

Detta laddar ner HTML-koden från sidan.

#### **2\. Skicka data (POST) till ett API:**

curl \-X POST https://api.example.com/login \-d "username=test\&password=1234"

Detta skickar ett POST-anrop med användarnamn och lösenord.

#### **3\. Skicka JSON-data:**

curl \-X POST https://api.example.com/users \\  
\-H "Content-Type: application/json" \\  
\-d '{"name": "Alice", "email": "[alice@example.com](mailto:alice@example.com)"}'

cURL körs från terminalen (eller kommandoprompten i Windows). Det följer detta grundformat:

curl \[alternativ\] \[URL\]

Vanliga alternativ:

X – specificerar HTTP-metod (GET, POST, PUT, DELETE)  
d – data att skicka  
H – header (t.ex. "Content-Type")

Varför är cURL bra att kunna?

Det är ett snabbt sätt att testa API-anrop utan att skriva kod  
Fungerar i alla operativsystem  
Används ofta av utvecklare, testare och DevOps