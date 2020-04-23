## How To Create A User Login Web System
Recently, I started work on a project where I had to figure out how to create a user login system to protect the website from unauthorized access. In this tutorial, I will show you how to make the same system using Python on Ubuntu Server 18.04.

### Seting Up Prereq Software
To begin, we recommend, regardless of the project or end goal to start by running the following command:
```
sudo apt-get update && sudo apt-get upgrade -y
```
and
```
sudo apt-get install cmake build-essential -y
```

After which you will need to install the Python Development software and a MySQL development client by running the following:
```
sudo apt-get install python python-pip python-dev libmysqlclient-dev python-mysql.connector python3-mysql.connector -y
```

Now we install MariaDB as our database where we will store our user's usernames and hashed passwords.
```
sudo apt-get install mariadb-server -y
```
Once install run ```sudo mysql``` so that we may setup a user, database, and table to connect our Python code to.
Now run:
```
CREATE USER 'chooseAUserName'@'localhost' IDENTIFIED BY 'chooseAPassword';
```
then,
```
GRANT ALL PRIVILEGES ON *.* TO 'chooseAUserName'@'localhost' WITH GRANT OPTION;
exit
```

Now we will install some Python libraries that we will need.
```
pip install flask
pip install flask-sqlalchemy
pip install flask-login
pip install passlib
```

### Seting Up Users

### Python Progamming

### HTML and CSS

### Trying Your Design
