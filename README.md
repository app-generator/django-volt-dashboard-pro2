# Django Volt Dashboard PRO

Django Dashboard coded with basic modules, database, ORM and deployment scripts on top of Volt Dashboard PRO (premium version), a modern Bootstrap dashboard design. Volt Pro is a premium Bootstrap 5 Admin Dashboard featuring over 800 components, 20 example pages and 10 fully customized plugin written in Vanilla Javascript.

- 👉 [Volt Dashboard PRO Django](https://appseed.us/product/volt-dashboard-pro/django/) - Product page
- 👉 [Volt Dashboard PRO Django](https://django-volt-enh.appseed-srv1.com/) - LIVE Demo
- 👉 [Complete documentation](https://docs.appseed.us/products/django-dashboards/volt-pro) - `Learn how to use and update the product`
  
<br />

> **Basic Version**

- `Up-to-date dependencies`, active versioning
- `Session-Based authentication`
- `Docker`

> **Extended Version** 

- `Authentication`
  - Social Login (optional) for Github & Twitter
  - Automatic suspension on failed logins 
  - Change Password, Self Deletion
- `Task Module`
  - Create, Delete and assign tasks 
- `Transactions Module`
  - Create, Delete and Edit Transactions 
- `Users Management` 
  - `Extended user profile`
  - Complete Users management (for `Admins`) 
    - Edit users, suspend/unsuspend

<br />

![Volt Dashboard PRO - Starter generated by AppSeed.](https://user-images.githubusercontent.com/51070104/172672843-8c40a801-3438-4e9c-86db-38a34191fbdf.png)

<br />

## ✨ Start the app in Docker

> **Step 1** - Download the [code](https://appseed.us/product/volt-dashboard-pro/django/) and unzip the sources (requires a `purchase`). 

```bash
$ # Get the code
$ unzip django-volt-dashboard-pro.zip
$ cd django-volt-dashboard-pro
```

<br />

> **Step 2** - Start the APP in `Docker`

```bash
$ docker-compose up --build 
```

Visit `http://localhost:5085` in your browser. The app should be up & running.

<br />

## ✨ How to use it

> Download the [code](https://appseed.us/product/volt-dashboard-pro/django/) and unzip the sources (requires a `purchase`). 

```bash
$ # Get the code
$ unzip django-volt-dashboard-pro.zip
$ cd django-volt-dashboard-pro
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

### 👉 Create Users

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
   |         |    |-- sidebar.html         # Sidebar component
   |         |    |-- footer.html          # App Footer
   |         |    |-- scripts.html         # Scripts common to all pages
   |         |
   |         |-- layouts/                   # Master pages
   |         |    |-- base-fullscreen.html  # Used by Authentication pages
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
Django Volt Dashboard PRO - Seed project generated by **[AppSeed Generator](https://appseed.us/generator/)**.
