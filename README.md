# Django Dev-Blog

## Purpose / Scope

This project serves to practice the fundamentals of Django development.  
For a walkthrough summary of the project, see [development steps](#development-steps).

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

9. Create a Django app:
    ```console
    python3 manage.py startapp posts
    ```

10. Create templates folder within app, static and media folders within root.  
    Create img folder within media, css, img and js folders within static.

11. Configure [settings.py](blog/settings.py) to include newly-created folders.

12. Create any required [models](posts/models.py) and templates e.g. [forms](posts/templates/forms.py).

13. If an ImageField is required:
    ```console
    pip3 install Pillow
    ```

14. Make migrations following those changes:
    ```console
    python3 manage.py makemigrations
    python3 manage.py migrate
    ```

15. Create your required [views](posts/views.py).

16. Create your app's required [URLs](posts/urls.py) and any necessary links to the overall project in your project's required [URLs](blog/urls.py).

17. Create your required [templates](posts/templates/blogposts.html).

18. Ensure the app is included in the INSTALLED_APPS list of the [settings.py](blog/settings.py) file.

19. Deploy to Heroku, include any environmental variables you require such as secret keys in the "Config Vars" section.

20. If using a postgreSQL database in Heroku, under the Resources tab add Heroku Postgres, copy the newly-created environmental variable to the local env.py file for testing.
