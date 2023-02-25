# Django-Tutorial
Learning Django Rest framework and building Api's
# Django FrameWork Brief
    1. A Django project contains many apps specific to it's purpose and each app contains
        admin.py, apps.py, models.py, tests.py, views.py and a migrations folder.
    2. Django uses MVC Architecture known as Model-View-Controller.
    3.

# Project setup:
    1. pip install django and django restframework
    2. create project by giving this commands
            django-admin startproject <poject_name>
            ex : django-admin startproject wisdompets
        explanation : This will create a package with asgi.py, settings.py, urls.py, wsgi.py
            
    3. Run the project by the below command 
            python manage.py runserver

    4. create Django App under same project by below command
            python manage.py startapp <app name>
            ex: python manage.py startapp adoptions
        explantion : This will create an app as above with admin.py, apps.py, models.py, tests.py, view.py

    5. Add the above app in settings.py file under installed apps 
        ex : settings.py line 40 inlcude withing 'installed_apps' list

    6. Once Model has been written, you need to migrate it by using this command under the project
                python manage.py makemigrations  
        to apply these migrations :  python manage.py migrate

    7. Since we dont have any data loaded in the db, we have pet_data.csv data to load in the resps db
        We have written a Python script to load the data into sqlite db
        by this command : python manage.py load_pet_data
    
    8. To create admin interface to pet data, we are creating super user by below command under app (wisdompets)
            1. python manage.py createsuperuser > username(bpraveen), password(wisdompets)


# Roles, Details and importance of files:
    1. manage.py : 
            This file is responsible for running our application.
        ex : python manage.py runserver

    2. apps.py : 
            app file controlls the settings specific to this app

    3. model.py :
            provides the dataLayer which Django uses to construct db schema and queries

    4. admin.py : 
            admin interface
    5. urls.py : 
            can be used for url routing specific to this app.
    
    6. views.py :
            Defines the logics and controll flow for handling the requests and defines the HTTP responses

    7. tests.py : 
            Can be used for writing the unittest for this app

    8. migrations : 
            This folder holds the files which django uses to migrate the databases as we create and change our db schema
            Once the Model has been created and you need to migrate the model
            command : python manage.py makemigrations

            

            