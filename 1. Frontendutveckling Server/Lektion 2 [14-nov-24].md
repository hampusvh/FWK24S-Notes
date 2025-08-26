npm init (initiera mappen som ett npm projekt)  
mkdir public src  
npm i express nodemon

const express \= require(‘express’)

const app \= express()  
const PORT \= 3000

app.get(‘/’, (req, res) \=\> {  
	res.json({message: ‘Hello’})  
})  
	res.sendFile(path.join(\_\_dirname, ‘../public/index.html’)}  
})

app.listen(PORT, () \=\> {  
	console.log(\`Server listening on port: ${PORT}\`)  
})

**Den här sektionen är väldigt viktig att lära sig och kunna utantill, förstå begreppen och koncepten. Man kan använda ChatGPT till sin fördel.** 

**API** \- Application Programming Interface

Ett API är ett sätt för olika program och tjänster att kommunicera med varandra och utbyta information. Tänk på API som en mellanhand eller "bro" som gör det möjligt för två olika system att kommunicera, även om de är olika.

**JSON** \- JavaScript Object Notation

JSON är ett enkelt sätt att organisera och skicka data så att olika program lätt kan förstå det. Man kan tänka på det som ett strukturerat sätt att skriva och paketera information. 