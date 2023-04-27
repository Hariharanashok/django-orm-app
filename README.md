# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:

An Django application is created inside dataproject folder.

### STEP 2:

A python program is written to create a table to store and retrieve data.

### STEP 3:

The table is created with 6 fields in which the username field is made as PrimaryKey.

### STEP 4:

Then the project files migrated. A superuser is also created.

### STEP 5:

Now the server side program is executed .

### STEP 6:

The admin page of our website is accessed using username and password.

### STEP 7:

Records are added and saved in the table inside the database.


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
