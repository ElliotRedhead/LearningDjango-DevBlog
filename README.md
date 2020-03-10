# Django Dev-Blog

## Purpose / Scope

This project serves to practice the fundamentals of Django development.  
For a walkthrough summary of the project, see [development steps](#development-steps)

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