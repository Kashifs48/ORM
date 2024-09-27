# Ex02 Django ORM Web Application
## Date: 

## AIM
To develop a Django application to store and retrieve data from a Bank database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![er_img](https://github.com/user-attachments/assets/1f477cf2-d9d0-4b75-97eb-b2bbaf50d212)


## DESIGN STEPS
STEP 1:
Clone the problem from GitHub

STEP 2:
Create a new app in Django project

STEP 3:
Enter the code for admin.py and models.py

STEP 4:
Execute Django admin and create details for 10 customers.

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 customers.

## PROGRAM

```
from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)
```

```
from django.db import models
from django.contrib import admin
class Employee (models.Model):
    eid=models.IntegerField(primary_key=True)
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()
 
class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')
```

## OUTPUT

![op_img](https://github.com/user-attachments/assets/7778de86-1ba9-484b-866d-9940f9f934ea)



## RESULT
Thus the program for creating a database using ORM hass been executed successfully
