## Django

The Django admin application can use your models to automatically build a site area that you can use to create, view,
update, and delete records. This can save you a lot of time during development, making it very easy to test your models
and get a feel for whether you have the right data.

ter registering the models we'll show how to create a new "superuser", login to the site, and create some books,
authors, book instances, and genres.

## Registering models

First, open admin.py in the catalog application (/locallibrary/catalog/admin.py). It currently looks like this â€” note
that it already imports django.contrib.admin:

    from django.contrib import admin
    
    # Register your models here.

Register the models by copying the following text into the bottom of the file. This code imports the models and then
calls admin.site.register to register each of them.

    from .models import Author, Genre, Book, BookInstance
    
    admin.site.register(Book)
    admin.site.register(Author)
    admin.site.register(Genre)
    admin.site.register(BookInstance)

## Creating a superuser

You can create a "superuser" account that has full access to the site and all needed permissions using manage.py.

Call the following command, in the same directory as manage.py, to create the superuser. You will be prompted to enter a
username, email address, and strong password.

    python3 manage.py createsuperuser

Once this command completes a new superuser will have been added to the database. Now restart the development server so
we can test the login:

    python3 manage.py runserver

## Advanced configuration
Django does a pretty good job of creating a basic admin site using the information from the registered models:

- Each model has a list of individual records, identified by the string created with the model's __str__() method, and
linked to detail views/forms for editing. By default, this view has an action menu at the top that you can use to
perform bulk delete operations on records.
- The model detail record forms for editing and adding records contain all the fields in the model, laid out vertically in
their declaration order.
- You can further customize the interface to make it even easier to use. Some of the things you can do are:

### List views:
- Add additional fields/information displayed for each record.
- Add filters to select which records are listed, based on date or some other selection value (e.g. Book loan status).
- Add additional options to the actions menu in list views and choose where this menu is displayed on the form.
### Detail views
- Choose which fields to display (or exclude), along with their order, grouping, whether they are editable, the widget
used, orientation etc.
- Add related fields to a record to allow inline editing (e.g. add the ability to add and edit book records while you're
creating their author record).



## Resources

[sources1](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Models)

[sources2](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Admin_site)

[sources3](https://simpleisbetterthancomplex.com/series/2017/09/11/a-complete-beginners-guide-to-django-part-2.html)
