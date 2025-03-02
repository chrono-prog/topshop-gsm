# Python Flask E-Commerce Website

A simple e-commerce website using Flask, Jinja2, SQLite, jQuery, Bootstrap and Python.

The application loads a gallery of devices that includes: image, name, price, and a small form to add devices to shopping cart. The device information is stored in a SQLite database and is displayed using Bootstrap's card class.

The application contains filters that were implemented through SQLite queries so that the user can scroll through the items according to different categories such as, Phones, Tablets, Laptops, Discounts etc.

The application can be visited here:

[https://topshopgsm.herokuapp.com/](https://topshopgsm.herokuapp.com/)


## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install the dependencies.

Go in the same directory as the requirements.txt file and run the following

```bash
pip install -r requirements.txt
```

## Usage

There are two ways to run the application the application

### Run as Python application 

Go to the same directory as the main application and run the following

```bash
python wsgi.py
```
### Run as Flask application 

Go to the same directory as the main application and run the following


```bash
set FLASK_APP=application.py
flask run
```


## Deploying on Heroku

The entry point to the application is in wsgi.py file

```python
from application import app

if __name__ == "__main__":
    app.run()
```
We then need to create a Procfile to deploy to Heroku



```bash
web: gunicorn wsgi:app
```

### Create the Heroku application

Use the HerokuCLI to deploy the application to Heroku 

```bash
heroku login
git init
heroku create topshopgsm
git add.
git commit -am "First python app"
git push heroku master
```

Once the files are deployed your application will be visible and can be visited. In our case the application is deployed at the link below:


[https://topshopgsm.herokuapp.com/](https://topshopgsm.herokuapp.com/)