# Django:



## Using Models

1- Django web applications access and manage data through Python objects refferred to as models.
2- Models define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, help text for documentation, label text for forms, etc.

## Designing the LocalLibrary models:

1- when designing your models it makes sense to have separate models for every "object" (a group of related information).
2- use models to represent selection-list options (e.g. like a drop down list of choices), rather than hard coding the choices inot the website itself.
3- use models to represent selection-list options(drop down list of choices), rather than hard coding the choices into the website itself.
4- Django allows you to define relationships that are one to one (OneToOneField), one to many (ForeignKey) and many to many (ManytoManyField).


## Model definition

***Models are usually defined in an application's models.py file. They are implemented as subclasses of django.db.models.Model,***
***and can include field, methods and metadata.***

## Typical model

from django.db import models

class MyModelName(models.Model): (A typical class defining a model, derived from the Model class.)

## Fields

1- A model can have an arbitrary number of fields, of any type - each one represents a column of data that we want to store in one of our database tables.
2- Each databe record (row) will consist of one of each field value.
3- my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')
4- Charfield means the field will contain strings and alphanumeric characters.

## Common Field Arguments

-help_text: provides a text label for HTML forms (like the admin stie).
-verbose_name: human-readable name for the field used in field labels.
-default: the default value for the field. This can be a value or a callable object.
-null: if True, Django will store blank values as NULL in the database for fields where this is appropiate.
-blank: if True, the field is allowed to be blank in your forms. The default is False, which means the django's form validation will force you to enter a value.
-choices: a group of choices for this field.
-primary_key: if True, sets the current firled as the primary key for the model. A primary key is a speical database column designated to uniquely identify all the diff table records.

## Common Field types: 

1- CharField: used to define short-to-mid sized fixed-length strings. You must specify the max_length of the data to be stored.
2- TextField: used for large arbitrary-length strings. You may specify a max_length for the field, but this is used only when the field is displayed in forms.
3- IntergerField: for storing interger (whole number) values, and for validating entered values as ints in forms.
4-DateField and DateTimeField: used for storing/rep dates and date/time info. Thsi fields can additionally declare the parameters auto_now = True (to set the field to the 
 current date every time the model is saved).
5- EmailField: used to store and validate email addy.
6- FileField: used to upload files and images. These have params to define how and where the uploaded files are stored.
7- AutoField: special type of int field that automatically increments. A primary key of this type is auto added to your model if you don't specify one.
8- ForeignKey: sued to specify a one-to-many relationship to antoher database model (a car has one manufactuer, but a manufactuer can make many cars.)
9- ManytoManyField: used to specify a many-to-many relationship (a book can have serveral genres, and each genre can contain several books.)

