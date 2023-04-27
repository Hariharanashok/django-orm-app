# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:

Create a new Django project using "django-admin startproject",get into the project's terminal and use "python3 manage.py startapp hospitalproject" command.

### STEP 2:

Define a model for the Hospitalapp in the models.py and allow host access and add the app name under the installed apps in settings.py

### STEP 3:

Register the models with the Django admin site. In admin.py under app folder, register the models with Django admin site.

## PROGRAM

```python

#IN Models.py:-

from django.db import models
from django.contrib import admin

# Create your models here.
class Student (models.Model):
    referencenumber=models.CharField(max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    bloodgroup=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()

class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','bloodgroup','age','email')

#IN Admin.py:-

from django.contrib import admin
from.models import Student,StudentAdmin

# Register your models here.
admin.site.register(Student,StudentAdmin)

```

## OUTPUT

![out1](https://user-images.githubusercontent.com/120353431/234791832-0e45e968-4d97-4938-acb2-734794ffbd62.png)


![out2](https://user-images.githubusercontent.com/120353431/234791921-7b7b0f0f-110b-4169-be25-55ffb9e07381.png)



## RESULT

Thus a Django application to store and retrieve data from a database using Object Relational Mapping(ORM) is developed.
