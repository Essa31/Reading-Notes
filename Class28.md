## Django: Working with forms

Django provieds a framework that allows developers to create forms and their fields, so you can use them as objects that can be generated as HTML forms to handle and validate user interactions.

But what are forms?

### Definition :

**Forms** are a flexible way to collect user input, as there are many widgets that can be used for entering many different data types, and in Django admin site they are mainly used for entering and modifying data in the database.

### HTML Forms:

Lets remember some things about HTML forms.

Forms in HTML are defined as a collection of elements inside `<form>â€¦</form>` tags. **ex**: ([source](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms#html_forms))

    <form action="/team_name_url/" method="post">
    <label for="team_name">Enter name: </label>
    <input id="team_name" type="text" name="name_field" value="Default name for team.">
    <input type="submit" value="OK">
    </form>

The submit button is used to get the user input and perform an action upon it.

### Django form handling process:

Django forms do the all everything that the normal HTML forms can do, which means that Django forms can:
- Display the default form to get the data for the first time.
- Recevie data from the user input and bind it to the form, so that if there is any error the from can be redisplayed.
- Clean and validate the data.
- Perform the required actions if all the data is valid.

Django also provides a class called `Form`, which can simplifies both generation of form HTML and data cleaning/validation.

### Declaring a Form:

Declaring a **Form** is just as simple as declaring a **Model** in Django. ex: ([source](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms#renew-book_form_using_a_form_and_function_view))

    from django import forms

    class RenewBookForm(forms.Form):
        renewal_date = forms.DateField(help_text="Enter a date between now and 4 weeks (default 3).")

The form uses the same kinds of fields that we can use when creating a model.



## Things I want to know more about

- None.

## Resources

[sources1](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms)

[sources2](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Home_page)

[sources3](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Generic_views)