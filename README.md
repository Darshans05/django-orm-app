# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![ER diagram](https://user-images.githubusercontent.com/115534676/230286348-477a4613-b465-48f4-b977-e8fa2837ade6.png)

## DESIGN STEPS

### STEP 1:
Create a django application using django-admin startapp in command line. Head to the application directory created inside the project directory. Open the models.py file. In models.py create two classes one defining the attributes and the other one defining attribute value types.

### STEP 2:
In the same directory, Head to admins.py and import the two classes from models.py that you have created earlier. Now register your created models in admins.py file and save both the files

### STEP 3:

Start the Django server and head over to admin page. Using the admin interface, you can add or delete data .

## PROGRAM
##File:Models.py:
``` python
from django.db import models
from django.contrib import admin


##Create your models here.
class Student (models.Model):
    referencenumber=models.CharField(max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()


class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email')
    
```
##File:Admin.py:
``` python
from django.contrib import admin
from .models import Student,StudentAdmin


# Register your models here.
admin.site.register(Student,StudentAdmin)

```

## OUTPUT
![web django-admin users](https://user-images.githubusercontent.com/115534676/230283388-0df23bf2-5d5c-4585-ae7f-840bd3ad77d9.png)


##VERIFYING PRIMARY-KEY
![web django users](https://user-images.githubusercontent.com/115534676/230283435-fe591ea8-0fca-40f2-8895-dec9eb75c792.png)

## RESULT
A Django application has been created that can be used to store and retrieve data from the database using Object Relational Mapping(ORM).
