# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![WhatsApp Image 2023-11-25 at 10 54 59_1a37d253](https://github.com/vikamuhan-reddy/django-orm-app/assets/144928933/c00093cf-8414-4227-9d0c-991fe638c526)


## DESIGN STEPS

### STEP 1:
Create ex02 directory.Then fork,clone the repository.Create a myapp.

### STEP 2:
Create a superuser admin. Then make migrate and migrate.
Make the changes in settings.

### STEP 3:
Write the models.py for creating a model named student and write the admin.py to register model.

### STEP 4:
Again migrate the code and run the code using runserver.

## PROGRAM
models.py 
```py
from django.db import models
from django.contrib import admin


class Student (models.Model):
    referencenumber=models.CharField(max_length=20,help_text="reference number",primary_key=True)
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    mobilenummber=models.IntegerField()


class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','mobilenumber')
```

admin.py
```py
from django.contrib import admin
from .models import Student,StudentAdmin


# Register your models here.
admin.site.register(Student,StudentAdmin)

```
## OUTPUT
![output](./web%20ex02.png)



## RESULT
we have successfully ten student user using ORM
