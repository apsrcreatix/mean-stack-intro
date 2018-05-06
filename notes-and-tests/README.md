# Important Notes

## For Ubuntu 16.04 users

### Steps for mongoDB

#### Import the public key used by the package management system

```sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5```

#### Create a list file for MongoDB

```echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.6 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.6.list```

#### Reload local package database

```sudo apt-get update```

#### Install the MongoDB packages

```sudo apt-get install -y mongodb-org```

### Run MongoDB Community Edition

#### Start MongoDB

```sudo service mongod start```

#### Verify that MongoDB has started successfully (should show a line **[initandlisten] waiting for connections on port 27017** )

```more /var/log/mongodb/mongod.log```

#### Stop MongoDB

```sudo service mongod stop```

#### Restart MongoDB

```sudo service mongod restart```

#### Begin using MongoDB

```mongo --host 127.0.0.1:27017```