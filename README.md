# [Material Kit](https://appseed.us/generator/material-kit/) Django

`Open-Source` seed project generated by AppSeed in **Django** Framework on top of **[Material Kit](https://appseed.us/generator/material-kit/)** design. Designed for those who like bold elements and beautiful websites, **Material Kit 2** is ready to help you create stunning websites and web apps. `Material Kit 2` is built with over 60 frontend individual elements, like buttons, inputs, navbars, nav tabs, cards, or alerts, giving you the freedom of choosing and combining.

- 👉 [Django Material Kit](https://appseed.us/product/material-kit/django/) - product page
- 👉 [Django Material Kit](https://django-material-kit.appseed-srv1.com/) - LIVE App
- 👉 [Complete documentation](https://docs.appseed.us/products/django-apps/material-kit) - `Learn how to use and update the product`
  - ✅ [Set up the environment](https://docs.appseed.us/products/django-apps/material-kit#environment)
  - ✅ [Start the app in Docker](https://docs.appseed.us/products/django-apps/material-kit#start-the-app-in-docker)
  - ✅ [Manual Build](https://docs.appseed.us/products/django-apps/material-kit#manual-build)
  - ✅ [Manage App Users](https://docs.appseed.us/products/django-apps/material-kit#manage-app-users)
  - ✅ [UI Assets and Templates](https://docs.appseed.us/products/django-apps/material-kit#ui-assets-and-templates)
  - ✅ [Set up the MySql Database](https://docs.appseed.us/products/django-apps/material-kit#set-up-the-mysql-database)
  - ✅ [Adding a new app](https://docs.appseed.us/products/django-apps/material-kit#adding-a-new-app)
  - ✅ [Static Assets for production](https://docs.appseed.us/products/django-apps/material-kit#static-assets-for-production)  

<br />

> Built with [Material Kit Generator](https://appseed.us/generator/material-kit/)
 
- Timestamp: `2022-06-16 09:44`
- Build ID: `f2b8eb1b-7cae-4700-93a9-a0c979916814`
- **Free [Support](https://appseed.us/support/)** (registered users) via `Email` and `Discord`

<br />

> Features

- `Up-to-date dependencies`
- Database: `mysql`
- UI-Ready app, Django Native ORM
- `Session-Based authentication`, Forms validation

<br />

![Material Kit - Starter generated by AppSeed.](https://user-images.githubusercontent.com/51070104/167396765-c88b7a95-155f-4236-8691-7b80fa2d9cd9.png)

<br />




## ✨ Set up the MySql Database

**Note:** Make sure your Mysql server is properly installed and accessible. 

> **Step 1** - Create the MySql Database to be used by the app

- `Create a new MySql` database
- `Create a new user` and assign full privilegies (read/write)

<br />

> **Step 2** - Edit the `.env` to match your MySql DB credentials. Make sure `DB_ENGINE` is set to `mysql`.

- `DB_ENGINE`  : `mysql` 
- `DB_NAME`    : default value = `appseed_db`
- `DB_HOST`    : default value = `localhost`
- `DB_PORT`    : default value = `3306`
- `DB_USERNAME`: default value = `appseed_db_usr`
- `DB_PASS`    : default value = `pass`

<br />

Here is a sample:  

```txt
# .env sample

DB_ENGINE=mysql             # Database Driver
DB_NAME=appseed_db          # Database Name
DB_USERNAME=appseed_db_usr  # Database User
DB_PASS=STRONG_PASS_HERE    # Password 
DB_HOST=localhost           # Database HOST, default is localhost 
DB_PORT=3306                # MySql port, default = 3306 
```

<br />


## ✨ How to use it

> Download the code 

```bash
$ # Get the code
$ git clone https://github.com/appseed-projects/f2b8eb1b-7cae-4700-93a9-a0c979916814.git
$ cd f2b8eb1b-7cae-4700-93a9-a0c979916814
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
   |              |-- 404-page.html         # 404 page
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



## ✨ PRO Version

> For more components, pages and priority on support, feel free to take a look at this amazing starter:

**Material Kit 2** is a premium design crafted by the `Creative-Tim` agency on top of Bootstrap 5 Framework. Designed for those who like bold elements and beautiful websites, Material Kit 2 is made of hundreds of elements, designed blocks, and fully coded pages built with an impressive level of quality.

- 👉 [Django Material Kit2 PRO](https://appseed.us/product/material-kit2-pro/django/) - product page
- 👉 [Django Material Kit2 PRO](https://django-material-kit2-pro.appseed-srv1.com/) - LIVE Demo

<br >

![Mk2 PRO - Premium Seed project by AppSeed.](https://user-images.githubusercontent.com/51070104/168224733-b054bb46-d454-4aea-bb94-2d01bf4760d2.png)

<br />

---
[Material Kit](https://appseed.us/generator/material-kit/) Django - Open-source starter generated by **[AppSeed Generator](https://appseed.us/generator/)**.
