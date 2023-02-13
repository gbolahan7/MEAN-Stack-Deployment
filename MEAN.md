# MEAN STACK DEPLOYMENT TO UBUNTU IN AWS

### This is the deployment of a book register form to Ubuntu server in AWS

## STEP 1 - Install NodeJS

### update ubuntu
`sudo apt update`

### upgrade ubuntu
`sudo apt upgrade`

### Add certificates and then install node
`sudo apt -y install curl dirmngr apt-transport-https lsb-release ca-certificates`

`curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -`

`sudo apt install -y nodejs`

## STEP 2 - Install MongoDB
`sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 0C49F3730359A14518585931BC711F9BA15703C6`

`echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.4.list`

`sudo apt install -y mongodb`

### Start the server and verify that the service is active
`sudo service mongodb start`

`sudo systemctl status mongodb`

![mongodb](/images/mongodb-run.PNG)

### Install NPM & body-parser package
`sudo apt install -y npm`

`sudo npm install body-parser`

### Create a folder 'Books' and initialize project
`mkdir Books && cd Books`

`npm init`

### Add a server.js file and insert code
`vi server.js`

![server](/images/server.PNG)


# Install Express and Set up routes to server

## Step 3 - Install Express and routes

`sudo npm install express mongoose`

### Mongoose is used to set up a schema for the database to store data for the book register

###  in books folder, Create apps folder and create route file
`mkdir apps && cd apps`

`vi routes.js`


### Next, create models folder in apps folder
`mkdir models && cd models`

### create file book.js and paste code
`vi book.js`
![book model](/images/book-model.PNG)

