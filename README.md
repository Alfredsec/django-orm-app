# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![web ex02](https://github.com/Alfredsec/django-orm-app/assets/120621608/725f1688-e816-4e75-bb86-3d89524f89c7)
## DESIGN STEPS

### STEP 1:
clone the repository from github.
### STEP 2:
create an admin interface for django
### STEP 3:
create an app and edit settings.py
### STEP 4:
make migrations and migrate the changes.
### STEP 5:
create admin user and write python code for admin and models.
### STEP 6:
make all the migrations to 'myapp'.
### STEP 7:
create an student database with 10 fields using runserver command.
## PROGRAM
### MODELS.PY
```
from django.db import models
from django.contrib import admin

# Create your models here.
class Student (models.Model):
    referencenumber=models.CharField(primary_key=True,max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    phoneno=models.IntegerField()

class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','phoneno')
```
### ADMIN.PY
```
from django.contrib import admin
from .models import Student,StudentAdmin


# Register your models here.
admin.site.register(Student,StudentAdmin)
```
## OUTPUT
### SERVER OUTPUT
![Screenshot 2023-05-27 163959](https://github.com/Alfredsec/django-orm-app/assets/120621608/5246afa5-df39-44ac-aa57-9b1462bf76a7)
### CLIENT OUTPUT 
![Screenshot 2023-05-27 042041](https://github.com/Alfredsec/django-orm-app/assets/120621608/416f2f84-5b9a-47b7-97e1-427de94e02a7)


## RESULT 
The program for creating an student database using ORM is executed sucessfully.
