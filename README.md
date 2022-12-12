"# Large_Flask_Application_blueprint" 


https://www.digitalocean.com/community/tutorials/how-to-structure-a-large-flask-application-with-flask-blueprints-and-flask-sqlalchemy

structure

flask_app

    ├── app
    │   ├── extensions.py
    │   ├── __init__.py
    │   ├── main
    │   │   ├── __init__.py
    │   │   └── routes.py
    │   ├── models
    │   │   ├── post.py
    │   │   └── question.py
    │   ├── posts
    │   │   ├── __init__.py
    │   │   └── routes.py
    │   ├── questions
    │   │   ├── __init__.py
    │   │   └── routes.py
    │   └── templates
    │       ├── base.html
    │       ├── index.html
    │       ├── posts
    │       │   ├── categories.html
    │       │   └── index.html
    │       └── questions
    │           └── index.html
    ├── app.db
    └── config.py

for windows use set and for ubuntu use export

set SECRET_KEY="your secret key"

set DATABASE_URI=postgresql://username:password@host:port/database_name <---------- double check

in flask_app folder

set FLASK_APP=app

set FLASK_ENV=development

flask shell

from app.extensions import db

from app.models.post import Post

db.create_all()

