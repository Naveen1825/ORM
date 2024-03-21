# Ex02 Django ORM Web Application
## Date: 20/3/2024

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![279274880-61384ad7-7a0f-4799-aaf9-32b7ec3f8913](https://github.com/Naveen1825/ORM/assets/138969868/32b7d99e-27ee-4e96-b30f-eb7691a184fc)

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM

model.py
```
from django.db import models
from django.contrib import admin
# Create your models here.

class Student(models.Model):
    referencenumber = models.CharField(max_length=10, help_text="Your Reference Nummber")
    name = models.CharField(max_length=100)
    age = models.IntegerField()
    email = models.EmailField()
    mobile_number = models.IntegerField()
    
class StudentAdmin(admin.ModelAdmin):
    list_display = ('referencenumber','name','age','email','mobile_number')

class Employee (models.Model):
    emp_id=models.CharField(primary_key=True,max_length=4,help_text=' Employee ID')
    ename=models.CharField(max_length=50)
    post=models.CharField(max_length=20)
    salary=models.IntegerField()

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('emp_id','ename','post','salary')
```

admin.py
```
from django.contrib import admin
from .models import Student,StudentAdmin,Employee,EmployeeAdmin

# Register your models here.
admin.site.register(Student,StudentAdmin)
admin.site.register(Employee,EmployeeAdmin)
```

## OUTPUT
![279271730-5cd5fde0-2250-43f5-9ead-f7d3bf612b54](https://github.com/Naveen1825/ORM/assets/138969868/0845dd2c-8be4-4434-91a4-650a2c7761a4)

## RESULT
Thus the program for creating a database using ORM hass been executed successfully
