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

![node install](/images/mongodb-run.PNG)

### Install NPM & body-parser package
`sudo apt install -y npm`

`sudo npm install body-parser`