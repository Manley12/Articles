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
Now that we have setup a few users let's write the Python code and go through what it does. Create a new file by running:
```
nano main.py
```
With the file open you can copy and paste or type yourself the following code:
```Python
from flask import Flask
from flask import Flask, flash, redirect, render_template, request, session, abort
from passlib.hash import sha256_crypt
import mysql.connector as mariadb
import os
import operator

app = Flask(__name__)

mariadb_connect = mariadb.connect(user='chooseAUserName', password='chooseAPassword', databse='Login')

@app.route('/')
def home():
  if not session.get('logged_in'):
    return render_template('login.html')
  else:
    return render_template('index.html')
    
@app.route('/login', methods=['POST'])
def do_admin_login():
  login = request.form
  
  userName = login['username']
  password = login['password']
  
  cur = mariadb_connect.cursor(buffered=True)
  data = cur.execute('SELECT * FROM Login WHERE username=%s', (userName))
  data = cur.fetchone()[2]
  
  if sha256_crypt.verify(password, data):
    account = True
    
  if account:
    session['logged_in'] = True
  else:
    flash('wrong password!')
  return home()
  
@app.route('logout')
def logout():
  session['logged_in'] = False
  return home()
  
if __name__ == "__main__":
  app.secret_key = os.urandom(12)
  app.run(debug=False,host='0.0.0.0', port=5000)
```

### HTML and CSS

### Trying Your Design
Now that you have the code written, we can run it and try it in our browser. Go ahead and run:
```
python main.py
```


Congratulations you have now created a user login system for a website in Python! You can now create your own website with private webpages where you may do things like keep a private journal, store your notes or other files, and much more. Let your imagination go wild and create something amazing.
