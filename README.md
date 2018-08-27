https://www.expressjs.com

https://www.handlebars.com

https://www.npmjs.com/package/hbs

nodemon server.js -e js,hbs

Static public files:
app.get('/',
    (req,res) => {
        // res.send('<h1>Hello Express!</h1>')
        res.send(
            {
                name: 'Andrew',
                likes: [
                    'Biking',
                    'Cities'
                ]
            }
        )
    }
)