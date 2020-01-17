bsawf.md

This repository contains the "bullet-proof" 4,000+ lines of source code to the UI of a dice-rolling betting game application.

The code was built while following <a target="_blank" href="https://buildasaasappwithflask.com/">Build a SaaS (web) Applications with Flask (and Docker)</a> (bsawf) 22-hour video course by full-stack developer <a target="_blank" href="https://www.NickJanetakis.com/uses">NickJanetakis.com</a> (<a target="_blank" href="htttps://twitter.com/nickjanetakis">@nickjanetakis</a>). <a target="_blank" href="https://www.youtube.com/watch?v=Q3arEfQ-pno&list=PL-v3vdeWVEsUDDWYgZ8ImfSORIHyrsBJy">VIDEO playlist</a>. BTW Nick also created and maintains <a target="_blank" href="https://www.youtube.com/watch?v=XeSD17YRijk&list=PL-v3vdeWVEsXT-u0JDQZnM90feU3NE3v8">a course on Docker</a>
and a podcast <a target="_blank" href="https://runninginproduction.com">Running in Production</a>.
Udemy.com?

## See the app with one command

The latest version of the completed app is at 
<a target="_blank" href="https://github.com/nickjj/build-a-saas-app-with-flask.git">
https://github.com/nickjj/build-a-saas-app-with-flask.git</a>

Unique to this website is a bash shell script I've written that enables you to run it on your MacOS laptop with one command.

1. View my script at:

   <pre><strong><a target="_blank" href="https://github.com/nickjj/build-a-saas-app-with-flask/blob/master/install-bsawf.sh">https://github.com/nickjj/build-a-saas-app-with-flask/blob/master/install-bsawf.sh</a>
   </strong></pre>

   This script is explained in the <a href="#ScriptExplained">section below</a>. 

1. Execute the script yourself by <strong>triple-clicking</strong> this command below:

   <pre><strong>bash -c "$(curl -fsSL https://raw.GitHubusercontent.com/nickjj/build-a-saas-app-with-flask/master/install-bsawf.sh)" -d -a -v 
   </strong></pre>

1. Open a Terminal on your mac, click on it, and keypress command+V to paste.

   The script should open the app in your default browser.   

   ![snakeeyes-landing-899x355](https://user-images.githubusercontent.com/300046/72588109-3e1ca980-38c5-11ea-965e-a935b8e69498.jpg)


<hr />

<a name="ScriptExplained"></a>

## Install Script Explained

In the script are comments of what responses looked like.



### The app

1. Open another Terminal to run <tt>tree</tt>. Here is the result:

   <pre>
├── Dockerfile
├── LICENSE
├── README.md
├── SnakeEyes_CLI.egg-info
│   ├── PKG-INFO
│   ├── SOURCES.txt
│   ├── dependency_links.txt
│   ├── entry_points.txt
│   ├── requires.txt
│   └── top_level.txt
├── assets
│   ├── app
│   │   ├── app.js
│   │   ├── app.scss
│   │   ├── modules
│   │   │   └── bootstrap.js
│   │   └── scss
│   │       ├── _forms.scss
│   │       ├── _nav.scss
│   │       ├── _sticky-footer.scss
│   │       ├── _typography.scss
│   │       ├── _variables-bootstrap.scss
│   │       ├── _variables.scss
│   │       └── all.scss
│   ├── package.json
│   ├── postcss.config.js
│   ├── static
│   │   ├── 502.html
│   │   ├── images
│   │   │   └── snake-eyes.jpg
│   │   ├── maintenance.html
│   │   └── robots.txt
│   ├── webpack.config.js
│   └── yarn.lock
├── cli
│   ├── __init__.py
│   ├── cli.py
│   └── commands
│       ├── __init__.py
│       ├── cmd_cov.py
│       ├── cmd_flake8.py
│       └── cmd_test.py
├── config
│   ├── __init__.py
│   ├── gunicorn.py
│   └── settings.py
├── docker-compose.override.example.yml
├── docker-compose.override.yml
├── docker-compose.yml
├── docker-entrypoint.sh
├── lib
│   ├── __init__.py
│   ├── flask_mailplus.py
│   └── tests.py
├── requirements.txt
├── setup.py
└── snakeeyes
    ├── __init__.py
    ├── app.py
    ├── blueprints
    │   ├── __init__.py
    │   ├── contact
    │   │   ├── __init__.py
    │   │   ├── forms.py
    │   │   ├── tasks.py
    │   │   ├── templates
    │   │   │   └── contact
    │   │   │       ├── index.html
    │   │   │       └── mail
    │   │   │           └── index.txt
    │   │   └── views.py
    │   └── page
    │       ├── __init__.py
    │       ├── templates
    │       │   └── page
    │       │       ├── home.html
    │       │       ├── privacy.html
    │       │       └── terms.html
    │       └── views.py
    ├── extensions.py
    ├── templates
    │   ├── layouts
    │   │   └── base.html
    │   └── macros
    │       ├── flash.html
    │       └── form.html
    └── tests
        ├── __init__.py
        ├── conftest.py
        ├── contact
        │   ├── __init__.py
        │   ├── test_tasks.py
        │   └── test_views.py
        └── page
            ├── __init__.py
            └── test_views.py
&nbsp;
26 directories, 70 files
   </pre>


## Technologies used

Different packages and libraries are mentioned in various files (assets folder), but they are here in <strong>alphabetical order</strong>:

* Ajax requests
* Babel
* Bash script<a target="_blank" href="https://nickjanetakis.com/blog/organize-your-text-based-notes-from-the-command-line-with-this-script">*</a>
* Bootstrap
* Celery
* CSRF Protection
* distutils.util (in config/settings.py)
* Docker Compose
* ES6 JS
* Flake8 to analyze Python code (in cli/commands/cmd_flake8.py)
* Flask
* Flask-Mail
* Fontawesome
* Gunicorn
* Jinga2
* JSON format files
* Node
* PostgreSQL persistant store
* Pytest package
* Redis cache
* Scss
* SQLAlchemy 
* Stripe microtransaction payments for subscriptions and coupon detection. It uses RESTFUL APIs.
* Yarn task runner
* Webpack (assets/webpack.config.js)
<br /><br />


## App Features

<a target="_blank" href="https://www.youtube.com/watch?v=qfXRpkLDZho">VIDEO</a>

* Coupon code
* Subscriptions
* Billing history
* Contact form
* Admin dashboard
* Search through a list of users
* [3:55] Edit details about each user
* Internationalization (i18n) 

## Not Features

* multi-tenancy

* RESTful APIs. However, Nick created a separate <a target="_blank" href="https://www.youtube.com/watch?v=s1xYgp9WHbU&list=PL-v3vdeWVEsUDDWYgZ8ImfSORIHyrsBJy&index=9">Mar 28, 2018 VIDEO</a> about building RESTful APIs.
* GraphQL
* Swagger/OpenAPI

## Course

The course's materials promises to show "the real (battle-hardened production) way to do it, without tedious research".

* Testing (using Pytest)
* CLI Script to "help manage your project" in cli/cli.py
* Web Sockets<a target="_blank" href="https://www.youtube.com/watch?v=5QUv14SQyjw&list=PL-v3vdeWVEsUDDWYgZ8ImfSORIHyrsBJy&index=11">*</a>


<a target="_blank" href="https://www.youtube.com/watch?v=Kq_khHWovl4&list=PL-v3vdeWVEsUDDWYgZ8ImfSORIHyrsBJy&index=12">3
Upgrading a Dockerized Flask App from Python 2.7 to Python 3.7.4</a> August 2019.
30:06


## Load

1. In a Terminal, run 

   <pre>e_modules/sass-loader/dist/cjs.js!./app/app.scss 249 KiB {mini-css-extract-plugin} [built]
webpack_1  |             + 12 hidden modules
worker_1   | [2020-01-17 04:59:42,036: INFO/Beat] beat: Starting...
   </pre>

   Press Ctrl+C to stop

1. Open another Terminal

## Create Another App

1. Change Nick's email in https://github.com/nickjj/build-a-saas-app-with-flask/blob/master/assets/static/502.html

## References

originally python:2.7-slim from DockerHub

https://www.youtube.com/watch?v=agXtLglF5Lw&list=PL-v3vdeWVEsUDDWYgZ8ImfSORIHyrsBJy&index=10


https://courses.nickjanetakis.com/courses/take/build-a-saas-app-with-flask/downloads/2295059-downloading-the-course-s-material
https://s3.amazonaws.com/thinkific-import-development/49114/bsawfcoursematerial-191204-142013.zip
exposed in https://github.com/JohnBobo/bsawf and https://github.com/jademount/bsawf and https://github.com/OprekAbleCom/bsawf-course-material

   * https://github.com/catsoap/bsawf

   * https://github.com/26huitailang/bsawf
   by Peter Chen 

   * https://github.com/ffaccia/snakeeyes

   * https://github.com/pulkit6559/Snakeeyes

   * https://github.com/dsazama/bsawf

   * https://github.com/tanujdave/bsawf

   * https://github.com/nandakumar92/bsawf

   * https://github.com/acuencadev/SnakeEyes (archived)


https://www.youtube.com/watch?v=5b8OiqQ6NuY&feature=youtu.be

unzip

06-creating-a-base-flask-app

docker-compose --build
    # uses 2.7-alpine

docker-compose stop


https://www.youtube.com/watch?v=5gu8wWX3Ob4
A Productive Linux Development Environment (WSL) on Windows with WSL, Docker, tmux, VSCode and More
Dec 21, 2018 [19:32]
https://www.youtube.com/watch?v=A0eqZujVfYU
Developing on Windows with WSL2 (Subsystem for Linux), VS Code, Docker, and the Terminal
by Scott Hanselman


https://www.youtube.com/watch?v=_ffYmnbm_wg
Live Demo: How to Begin Writing Tests in an Untested Code Base