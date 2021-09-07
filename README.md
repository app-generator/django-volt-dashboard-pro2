# [Django Dashboard](http://appseed.us/admin-dashboards/django) - Volt Bootstrap 5 PRO

**Django Dashboard** coded with basic modules, database, ORM and deployment scripts on top of **[Volt Dashboard PRO](https://docs.appseed.us/bootstrap-template/volt-dashboard-pro/)** (premium version), a modern Bootstrap dashboard design. Volt Pro is a premium Bootstrap 5 Admin Dashboard featuring over 800 components, 20 example pages and 10 fully customized plugin written in Vanilla Javascript. 

<br />

## [Django Dashboard](http://appseed.us/admin-dashboards/django) Features

- UI Kit: **Volt Dashboard PRO** by **Themesberg**
- Codebase - [Django Dashboard Boilerplate](https://docs.appseed.us/boilerplate-code/django-dashboard)
- UI-Ready app, SQLite Database, Django Native ORM
- Modular design, best practices codebase
- Session-Based Authentication, Forms validation
- Deployment scripts: Docker, Gunicorn/Nginx
- Support via Github (issues tracker) and [Discord](https://discord.gg/fZC6hup) - 24/7 LIVE Service.

<br />

> Links

- [Django Volt PRO](https://appseed.us/admin-dashboards/django-dashboard-volt-pro) - product page
- [Django Volt PRO](https://django-volt-pro.appseed-srv1.com/) - LIVE deployment
- [Django Volt PRO](https://docs.appseed.us/products/django-dashboards/volt-pro) - product documentation

<br />

## **[Volt Dashboard PRO](https://docs.appseed.us/bootstrap-template/volt-dashboard-pro/)**

Volt Pro is a premium Bootstrap 5 Admin Dashboard featuring over 800 components, 20 example pages and 10 fully customized plugin written in Vanilla Javascript.

**800+ Components, 20 Example Pages** - There are more than 800 premium Bootstrap 5 components included with the admin dashboard, some of which are buttons, forms, alerts, datepickers, range sliders and many more. Volt Pro comes with 20 example pages including the overview page, messages, user settings, transactions, calendar, sign in, sign up, and many more pages.

**10 Lightweight Plugins** - There are at least 10 lightweight Vanilla JS plugin libraries that we have customized and expanded in terms of features that you can use for your application. Some of these are a calendar, SVG maps, datepickers, notifications, drag and drop file uploads and many more.

- [Product Page](https://themesberg.com/product/admin-dashboard/volt-premium-bootstrap-5-dashboard) - hosted by [Themesberg](https://appseed.us/agency/themesberg)
- [Product Docs - Quick Start](https://themesberg.com/docs/volt-bootstrap-5-dashboard/getting-started/quick-start/) - official product documentation

<br />

![Django Dashboard Volt PRO - Template project provided by AppSeed.](https://raw.githubusercontent.com/app-generator/django-dashboard-volt-pro/main/media/django-dashboard-volt-pro-intro.gif)

<br />

## How to use it

```bash
$ # Get the code
$ git clone https://github.com/app-generator/priv-django-dashboard-volt-pro.git
$ cd priv-django-dashboard-volt-pro
$
$ # Virtualenv modules installation (Unix based systems)
$ virtualenv env
$ source env/bin/activate
$
$ # Virtualenv modules installation (Windows based systems)
$ # virtualenv env
$ # .\env\Scripts\activate
$
$ # Install modules - SQLite Storage
$ pip3 install -r requirements.txt
$
$ # Create tables
$ python manage.py makemigrations
$ python manage.py migrate
$
$ # Start the application (development mode)
$ python manage.py runserver # default port 8000
$
$ # Start the app - custom port
$ # python manage.py runserver 0.0.0.0:<your_port>
$
$ # Access the web app in browser: http://127.0.0.1:8000/
```

> Note: To use the app, please access the registration page and create a new user. After authentication, the app will unlock the private pages.

<br />

## Code-base structure

The project is coded using a simple and intuitive structure presented below:

```bash
< PROJECT ROOT >
   |
   |-- core/                               # Implements app logic and serve the static assets
   |    |-- settings.py                    # Django app bootstrapper
   |    |-- wsgi.py                        # Start the app in production
   |    |-- urls.py                        # Define URLs served by all apps/nodes
   |    |
   |    |-- static/
   |    |    |-- <css, JS, images>         # CSS files, Javascripts files
   |    |
   |    |-- templates/                     # Templates used to render pages
   |         |
   |         |-- includes/                 # HTML chunks and components
   |         |    |-- navigation.html      # Top menu component
   |         |    |-- sidebar.html         # Sidebar component
   |         |    |-- footer.html          # App Footer
   |         |    |-- scripts.html         # Scripts common to all pages
   |         |
   |         |-- layouts/                  # Master pages
   |         |    |-- base-fullscreen.html # Used by Authentication pages
   |         |    |-- base.html            # Used by common pages
   |         |
   |         |-- accounts/                 # Authentication pages
   |         |    |-- login.html           # Login page
   |         |    |-- register.html        # Register page
   |         |
   |      index.html                       # The default page
   |     page-404.html                     # Error 404 page
   |     page-500.html                     # Error 404 page
   |       *.html                          # All other HTML pages
   |
   |-- apps/
   |    |-- authentication/                # Handles auth routes (login and register)
   |    |    |
   |    |    |-- urls.py                   # Define authentication routes  
   |    |    |-- views.py                  # Handles login and registration  
   |    |    |-- forms.py                  # Define auth forms  
   |    |
   |    |-- app/                           # A simple app that serve HTML files
   |         |
   |         |-- views.py                  # Serve HTML pages for authenticated users
   |         |-- urls.py                   # Define some super simple routes  
   |
   |-- requirements.txt                    # Development modules - SQLite storage
   |
   |-- .env                                # Inject Configuration via Environment
   |-- manage.py                           # Start the app - Django default start script
   |
   |-- ************************************************************************
```

<br />

> The bootstrap flow

- Django bootstrapper `manage.py` uses `core/settings.py` as the main configuration file
- `core/settings.py` loads the app magic from `.env` file
- Redirect the guest users to Login page
- Unlock the pages served by *app* node for authenticated users

<br />

## Recompile CSS

To recompile SCSS files, follow this setup:

<br />

**Step #1** - Install tools

- [NodeJS](https://nodejs.org/en/) 12.x or higher
- [Gulp](https://gulpjs.com/) - globally 
    - `npm install -g gulp-cli`
- [Yarn](https://yarnpkg.com/) (optional) 

<br />

**Step #2** - Change the working directory to `assets` folder

```bash
$ cd app/base/static/assets
```

<br />

**Step #3** - Install modules (this will create a classic `node_modules` directory)

```bash
$ npm install
// OR
$ yarn
```

<br />

**Step #4** - Edit & Recompile SCSS files 

```bash
$ gulp
```

The generated files (css, min.css) are saved in `static/assets/css` directory.

<br />

## Deployment

The app is provided with a basic configuration to be executed in [Docker](https://www.docker.com/), [Gunicorn](https://gunicorn.org/), and [Waitress](https://docs.pylonsproject.org/projects/waitress/en/stable/).

### [Docker](https://www.docker.com/) execution
---

The application can be easily executed in a docker container. The steps:

> Get the code

```bash
$ git clone https://github.com/app-generator/priv-django-dashboard-volt-pro.git
$ cd priv-django-dashboard-volt-pro
```

> Start the app in Docker

```bash
$ sudo docker-compose pull && sudo docker-compose build && sudo docker-compose up -d
```

Visit `http://localhost:85` in your browser. The app should be up & running.

<br />

### [Gunicorn](https://gunicorn.org/)
---

Gunicorn 'Green Unicorn' is a Python WSGI HTTP Server for UNIX.

> Install using pip

```bash
$ pip install gunicorn
```
> Start the app using gunicorn binary

```bash
$ gunicorn --bind=0.0.0.0:8001 core.wsgi:application
Serving on http://localhost:8001
```

Visit `http://localhost:8001` in your browser. The app should be up & running.


<br />

### [Waitress](https://docs.pylonsproject.org/projects/waitress/en/stable/)
---

Waitress (Gunicorn equivalent for Windows) is meant to be a production-quality pure-Python WSGI server with very acceptable performance. It has no dependencies except ones that live in the Python standard library.

> Install using pip

```bash
$ pip install waitress
```
> Start the app using [waitress-serve](https://docs.pylonsproject.org/projects/waitress/en/stable/runner.html)

```bash
$ waitress-serve --port=8001 core.wsgi:application
Serving on http://localhost:8001
```

Visit `http://localhost:8001` in your browser. The app should be up & running.

<br />

## Credits & Links

- [Django](https://www.djangoproject.com/) - The official website
- [Boilerplate Code](https://appseed.us/boilerplate-code) - Index provided by **AppSeed**
- [Boilerplate Code](https://github.com/app-generator/boilerplate-code) - Index published on Github

<br />

---
[Django Dashboard Volt](https://appseed.us/admin-dashboards/django-dashboard-volt-pro) - Provided by **AppSeed** [App Generator](https://appseed.us/app-generator).
