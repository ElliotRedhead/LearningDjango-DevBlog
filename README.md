# Django Dev-Blog

## Purpose / Scope

This project serves to practice the fundamentals of Django development.  
For a walkthrough summary of the project, see [development steps](#development-steps)

[![Build Status](https://travis-ci.org/ElliotRedhead/Django-DevBlog.svg?branch=master)](https://travis-ci.org/ElliotRedhead/Django-DevBlog)

## Development Steps

Console commands will vary throughout based on OS.

1. Install your chosen version of Django:  
    ```console
    pip3 install django==1.11.24
    ```

2. Create a Django project:
    ```console
    django-admin startproject blog .
    ```

3. Initialise database and prepare tables:
    ```console
    python3 manage.py migrate
    ```

4. Run the server.
    ```console
    python3 manage.py runserver
    ```

5. Add non-required files to [.gitignore](.gitignore):
    ```
    __pycache__
    *.sqlite3
    ```

6. Toggle switch for target repo on [Travis-CI](https://travis-ci.org/account/repositories).

7. Copy markdown in build status of the target repo.

8. Create and populate [.travis.yml](.travis.yml).