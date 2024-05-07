~~~
Ex02 Django ORM Web Application

Date: 1.04.2024

AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

Entity Relationship Diagram
~~~
![image](https://github.com/niranjanadevi-s/ORM/assets/141748873/af034ba2-5226-46b2-aafe-94a0d08a1589)
~~~
DESIGN STEPS
STEP 1:Clone the problem from GitHub
STEP 2:Create a new app in Django project
STEP 3:Enter the code for admin.py and models.py
STEP 4:Execute Django admin and create details for 10 books
PROGRAM

admin.py

from django.contrib import admin
from .models import railway,railwayAdmin
admin.site.register(railway,railwayAdmin)

models.py

from django.db import models
from django.contrib import admin
class railway (models.Model):
    train_code=models.CharField(max_length=20,help_text="railway train_code")(primary_key=True)
    train_name=models.CharField(max_length=100)
    start_time=models.IntegerField()
    End_time=models.IntegerField()
    start_station_code=models.IntegerField()
    end_station_code=models.IntegerField()
    
 
class railwayAdmin(admin.ModelAdmin):
    list_display=('train_code','train_name','start_time','End_time','start_station_code','end_station_code',)
~~~
## OUTPUT

![image](https://github.com/niranjanadevi-s/ORM/assets/141748873/e069375c-0f91-4ac4-8b95-c16d1c9870b4)

## RESULT
Thus the program for creating a database using ORM hass been executed successfully
