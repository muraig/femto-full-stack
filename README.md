# Femto Full Stack Project Generator

Quickly build web application stack (for prototyping - but not only - or for learning concepts) based on FastAPI and SQLite for the backend and Svelte and Tailwindcss for the frontend.

## Background

My meeds: experiments and learn ! From this template ^[https://github.com/tiangolo/full-stack-fastapi-postgresql], I spent many hours analyzing tons of code and reading thousands of pages of documentation to better understand the concepts! So, I decided to simplify as much as possible and only keep what I needed. Here is the partial result! I hope my work will help you!

Note on *partial*: As backend is "complete" (remove code is easy!), frontend is'nt! Due to the complete rewrite from Vue/Vuetify to Svelte/Tailwind.

## App Features

In his near future state, this model will offer some basic, but still important features:

As "super" admin:

- I want to list registered users
- I want to update my profile
- I want to update user profile
- I want to deactivate an user
- I want to change user role
- I want to update app settings

As "normal" user:

- I want to Register a new account if authorized by app
- I want to log in
- I want to see my profile details
- I want to update my profile
- I want to change my password
- I want to recover my password if I lost it

## Technical Features

- Backend
    - [FastAPI](https://github.com/tiangolo/fastapi): A Python framework "FastAPI framework, high performance, easy to learn, fast to code, ready for production" and its excellent [documentation](https://fastapi.tiangolo.com/)
    - [SQLite](https://sqlite.org/index.html): "SQLite is a C-language library that implements a small, fast, self-contained, high-reliability, full-featured, **SQL database engine**"
    - [SQLAlchemy](https://www.sqlalchemy.org/): "SQLAlchemy is the Python SQL toolkit and **Object Relational Mapper** that gives application developers the full power and flexibility of SQL.".
    - [Poetry](https://python-poetry.org/): "Python packaging and dependency management made easy".
- Frontend
    - [Svelte](https://github.com/sveltejs/svelte): "Svelte is a new way to build web applications. It's a **compiler** that takes your declarative components and converts them into efficient JavaScript that surgically updates the DOM.".
    - [Tailwindcss](https://github.com/tailwindlabs/tailwindcss): "A utility-first **CSS framework** for rapidly building custom user interfaces.".
    - [nvm](https://github.com/nvm-sh/nvm): A node version manager.

## How to use it

Before starting, you should have *python3*, *poetry* and *nvm* globally installed

Open your favorite terminal, go to your base project directory then run:

```zsh
pip install cookiecutter # Once!
cookiecutter https://github.com/ffvpor/femto-full-stack.git
```

### Input variables

- ```project_name```: The name of the project.
- ```project_blueprint``` :
- ```project_short_description```: Few words about your project.
- ```domain_main```: For future project deployment in production.
- ```backend_cors_origins```: Enabled domains (Origin) for CORS (Cross Origin Resource Sharing) to allow communication between backend and frontend.
- ```secret_key```: Used by backend to "protect" sensible data.
- ```first_superuser```: Act as administrator to manage users and app.
- ```first_superuser_password```: Administrator password, **strong** as possible.
- ```sqlalchemy_database_uri```: The connection string to SQLite. By default, "sqlite:///./app/app.db".

Use command below -- in another terminal -- to generate password and secret keys as asked:

```zsh
$ openssl rand -hex 32
# Outputs something like: c3cbd330748fa67f39989b601ba04411164153646c9b5445c65cf5404580b2dc
```
