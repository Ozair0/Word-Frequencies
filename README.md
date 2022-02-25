# NodeJS(Express) Word Frequencies

# -- Setup --
### install npm dependencies
<code>npm install</code>

# -- Run --
<code>npm run serve</code>

# -- Input ---
### In request header Content-Type is required to be application/json and Body should be type JSON
### App takes 2 inputs text and k
### text: is the text you want to send max amount is 1GB(Can be changed in app)
### k: is the number of unique words you want in the text
### Example:
#### Request
Header Content-Type: application/json <br/>
Body(JSON): <pre>{
    "text":"test Test home Home Work work no no yes yes NO NO",
    "k": 4
}</pre>

#### Response
<pre>
{
    "frequencies": [
        {
            "word": "no",
            "count": 4
        },
        {
            "word": "test",
            "count": 2
        },
        {
            "word": "home",
            "count": 2
        },
        {
            "word": "work",
            "count": 2
        }
    ]
}</pre>