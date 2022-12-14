# [Django & MySql](https://github.com/app-generator/sample-docker-django-mysql) `Docker Sample`  

`Open-Source` seed project provided by AppSeed in **Django** Framework on top of **[Material Kit](https://appseed.us/product/material-kit/django/)** design. Designed for those who like bold elements and beautiful websites, **Material Kit 2** is ready to help you create stunning websites and web apps. `Material Kit 2` is built with over 60 frontend individual elements, like buttons, inputs, navbars, nav tabs, cards, or alerts, giving you the freedom of choosing and combining.

- 👉 [Django Material Kit](https://appseed.us/product/material-kit/django/) - product page
- 👉 [Django Material Kit](https://django-material-kit.appseed-srv1.com/) - LIVE App
  
<br />

## [Black Friday](https://appseed.us/discounts/) - `75%OFF`

> The campaign is active until `30.NOV` and applies to all products and licenses.

[![AppSeed - Black Friday 2022 Campaign, 75% OFF Discount (all products).](https://user-images.githubusercontent.com/51070104/201829599-9fe6bdd7-3f19-46f3-9115-962eeb13bf29.jpg)](https://appseed.us/discounts/)

<br />

> 🚀 Built with [App Generator](https://appseed.us/generator/), Timestamp: `2022-09-18 07:49`

- ✅ `Up-to-date dependencies`
- ✅ UI-Ready app, Django Native ORM
- ✅ `Session-Based authentication`, Forms validation
- ✅ `Docker`: bundled with `MySql`
  - `LIVE-reload` on changes

<br />

![Material Kit - Starter generated by AppSeed.](https://user-images.githubusercontent.com/51070104/167396765-c88b7a95-155f-4236-8691-7b80fa2d9cd9.png)

<br />

## ✨ Start in `Docker`

**Note**: Make sure the PORT `3306` is free (usually reserved by the local MySql instance). 

> 👉 **Step 1** - Download the code from the GH repository (using `GIT`) 

```bash
$ git clone https://github.com/app-generator/sample-docker-django-mysql.git
$ cd sample-docker-django-mysql
```

<br />

> 👉 **Step 2** - Start the APP in `Docker`

```bash
$ docker-compose up --build 
```

<br />

> 👉 **Step 3** - `Migrate DB`

```bash
$ docker-compose run --rm appseed-app python manage.py makemigrations
$ docker-compose run --rm appseed-app python manage.py migrate
```

<br />

> 👉 **Step 4** - Create `Superuser`

```bash
$ docker-compose run --rm appseed-app python manage.py createsuperuser
```

<br />

> 👉 **Step 5** - Access the `APP`

Visit `http://localhost:5085` in your browser. The app should be up & running.

<br />

## ✨ Manual Build

> Download the code 

```bash
$ # Get the code
$ git clone https://github.com/app-generator/sample-docker-django-mysql.git
$ cd sample-docker-django-mysql
```

<br />

### 👉 Set Up for `Unix`, `MacOS` 

> Install modules via `VENV`  

```bash
$ virtualenv env
$ source env/bin/activate
$ pip3 install -r requirements.txt
```

<br />

> Set Up Database

```bash
$ python manage.py makemigrations
$ python manage.py migrate
```

<br />

> Start the app

```bash
$ python manage.py runserver
```

At this point, the app runs at `http://127.0.0.1:8000/`. 

<br />

### 👉 Set Up for `Windows` 

> Install modules via `VENV` (windows) 

```
$ virtualenv env
$ .\env\Scripts\activate
$ pip3 install -r requirements.txt
```

<br />

> Set Up Database

```bash
$ python manage.py makemigrations
$ python manage.py migrate
```

<br />

> Start the app

```bash
$ python manage.py runserver
```

At this point, the app runs at `http://127.0.0.1:8000/`. 

<br />

## ✨ Create Users

By default, the app redirects guest users to authenticate. In order to access the private pages, follow this set up: 

- Start the app via `flask run`
- Access the `registration` page and create a new user:
  - `http://127.0.0.1:8000/register/`
- Access the `sign in` page and authenticate
  - `http://127.0.0.1:8000/login/`

<br />

## ✨ Code-base structure

The project is coded using a simple and intuitive structure presented below:

```bash
< PROJECT ROOT >
   |
   |-- core/                               # Implements app configuration
   |    |-- settings.py                    # Defines Global Settings
   |    |-- wsgi.py                        # Start the app in production
   |    |-- urls.py                        # Define URLs served by all apps/nodes
   |
   |-- apps/
   |    |
   |    |-- home/                          # A simple app that serve HTML files
   |    |    |-- views.py                  # Serve HTML pages for authenticated users
   |    |    |-- urls.py                   # Define some super simple routes  
   |    |
   |    |-- authentication/                # Handles auth routes (login and register)
   |    |    |-- urls.py                   # Define authentication routes  
   |    |    |-- views.py                  # Handles login and registration  
   |    |    |-- forms.py                  # Define auth forms (login and register) 
   |    |
   |    |-- static/
   |    |    |-- <css, JS, images>         # CSS files, Javascripts files
   |    |
   |    |-- templates/                     # Templates used to render pages
   |         |-- includes/                 # HTML chunks and components
   |         |    |-- navigation.html      # Top menu component
   |         |    |-- footer.html          # App Footer
   |         |    |-- scripts.html         # Scripts common to all pages
   |         |
   |         |-- layouts/                   # Master pages
   |         |    |-- base.html             # Used by common pages
   |         |
   |         |-- accounts/                  # Authentication pages
   |         |    |-- login.html            # Login page
   |         |    |-- register.html         # Register page
   |         |
   |         |-- home/                      # UI Kit Pages
   |              |-- index.html            # Index page
   |              |-- page-404.html         # 404 page
   |              |-- *.html                # All other pages
   |
   |-- requirements.txt                     # Development modules - SQLite storage
   |
   |-- .env                                 # Inject Configuration via Environment
   |-- manage.py                            # Start the app - Django default start script
   |
   |-- ************************************************************************
```

<br />

---
[Django & MySql](https://github.com/app-generator/sample-docker-django-mysql) `Docker Sample`  - Open-source starter provided by **[AppSeed Generator](https://appseed.us/generator/)**.
