## Twitoff
A web application for comparing Twitter users

## Installation
Downloaded repo and navigated there fromt he command line

```sh
git clone: repo_name

cd dir
```

## setup
```sh
pipenv --python 3.7
pipenv install pandas
pipenv install Flask Flask-SQLAlchemy Flask-Migrate
pipenv shell
```

## Creating and migrating the database:
note: Windows users can omit the "FLASK_APP=web_app" part...

```sh
FLASK_APP=web_app flask db init #> generates app/migrations dir

# run both when changing the schema:
FLASK_APP=web_app flask db migrate #> creates the db (with "alembic_version" table)
FLASK_APP=web_app flask db upgrade #> creates the specified tables
```

## To run: 
from pipenv shell: 
```sh
FLASK_APP=web_app flask run
```

## To open database in tableplus
1. New connection
2. SQLite
3. Copy Path from .db file
4. use that path for the SQLite path