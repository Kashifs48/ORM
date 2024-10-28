# Ex02 Django ORM Web Application
## Date: 28-10-2024

## AIM
To develop a Django application to store and retrieve data from a Bank database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![image](https://github.com/user-attachments/assets/595098ee-df6a-483b-a14a-cb4a8f43762a)



## DESIGN STEPS

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
from .models import Loan

@admin.register(Loan)
class LoanAdmin(admin.ModelAdmin):
    list_display = ('loan_id', 'customer_name', 'amount', 'interest_rate', 'duration_months', 'start_date')
    search_fields = ('customer_name', 'loan_id')Admin)
```

```
from django.db import models

class Loan(models.Model):
    loan_id = models.AutoField(primary_key=True)  # Auto incrementing primary key
    customer_name = models.CharField(max_length=100)
    address = models.CharField(max_length=255)
    phone_number = models.CharField(max_length=15)
    email = models.EmailField()
    amount = models.DecimalField(max_digits=10, decimal_places=2)
    interest_rate = models.FloatField()
    duration_months = models.PositiveIntegerField()
    start_date = models.DateField()

    def __str__(self):
        return f"Loan ID: {self.loan_id} - {self.customer_name}"
```

## OUTPUT

![image](https://github.com/user-attachments/assets/52c36bca-eec4-4d6e-9f8e-c149a941da19)




## RESULT
Thus the program for creating a database using ORM hass been executed successfully
