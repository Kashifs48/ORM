# Ex02 Django ORM Web Application
## Date: 4-11-2024

## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM
![Screenshot 2024-11-04 142255](https://github.com/user-attachments/assets/586a92e2-5b99-4e59-aef1-ef5e59821ce9)


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
```
models.py

from django.db import models
from django.contrib import admin
class bankloan (models.Model):
    Name=models.CharField(max_length=20)
    accno=models.CharField(max_length=20,primary_key=True)
    loanid=models.IntegerField()
    amount=models.IntegerField()
    ifsccode=models.CharField(max_length=11)

class bankloanAdmin(admin.ModelAdmin):
        list_display=('Name','accno','loanid','amount','ifsccode')

admin.py

from django.contrib import admin
from.models import bankloan,bankloanAdmin
admin.site.register(bankloan,bankloanAdmin)
```
## OUTPUT

![Screenshot 2024-11-04 142310](https://github.com/user-attachments/assets/dad6afd8-c8ea-4dcc-8efd-6f534e8a7f22)



## RESULT
Thus the program for creating a database using ORM hass been executed successfully
