**Axios** 

const bodyParser \= require('body-parser');  
const express \= require('express');  
const axios \= require('axios');

const app \= express();  
const PORT \= 3000;

app.use(bodyParser.urlencoded({ extended: true }));

app.get('/', async (req, res) \=\> {  
  try {  
    const response \= await axios.get('...', {  
      headers: {  
        'X-Api-Key': 'din-api-nyckel'  
      }  
    });  
    const result \= response.data;  
    res.json(result);  
  } catch (error) {  
    console.error(error);  
    res.status(500).send('Något gick fel\!');  
  }  
});

app.listen(PORT, () \=\> {  
  console.log(\`Listening on port: ${PORT}\`);  
});

**Put** \- Uppdaterar en hel resurs

**Patch** \- Uppdaterar endast en del av en resurs

