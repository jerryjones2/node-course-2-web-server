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

git instructions
===============================
go to root folder of project
git init
ls -a
git add README.md
git add package.json
git add public/
git add server.js
git add views/

create .gitignore
node_modules/
package-lock.json
server.log

git add .gitignore

git commit
------------------------------
https://help.github.com/enterprise/2.14/user/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/
ls -al ~/.ssh  <-- check to see if you have a ssh key
ssh-keygen -t rsa -b 4096 -C "jerryjones2@gmail.com"

start ssh server:
eval "$(ssh-agent -s)"

ssh-add -K ~/.ssh/id_rsa

pbcopy < ~/.ssh/id_rsa.pub

test that the ssh key was installed ok:
ssh -T git@github.com

git remote add origin https://github.com/jerryjones2/node-course-2-web-server.git
git push -u origin master

Heroku
========================
https://toolbelt.heroku.com
jerryjones2@gmail.com

add ssh key
heroku keys:add

to remove: heroku keys:remove jerryjones2@gmail.com

to connect heroku to git:
ssh -v git@heroku.com

add to package.json:
"start":"node server.js"

commit changes files:
git add .
git commit -m 'Setup start script and heroku port'