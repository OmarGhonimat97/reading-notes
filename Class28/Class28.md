# Readings: Django CRUD and Forms

## Django Forms

An HTML Form is a group of one or more fields/widgets on a web page, which can be used to collect information from users for submission to a server. Forms are a flexible mechanism for collecting user input because there are suitable widgets for entering many different types of data, including text boxes, checkboxes, radio buttons, date pickers and so on. Forms are also a relatively secure way of sharing data with the server, as they allow us to send data in POST requests with cross-site request forgery protection.

### HTML Forms

A form may have any number of other input elements and their associated labels.

The form attributes define the HTTP method used to send the data and the destination of the data on the server (action):

> action: The resource/URL where data is to be sent for processing when the form is submitted. If this is not set (or set to an empty string), then the form will be submitted back to the current page URL.

> method: The HTTP method used to send the data: post or get.
- The POST method should always be used if the data is going to result in a change to the server's database, because it can be made more resistant to cross-site forgery request attacks.
- The GET method should only be used for forms that don't change user data (for example, a search form). It is recommended for when you want to be able to bookmark or share the URL.

### Django form handling process

Django's form handling uses these techniques: the view gets a request, performs any actions required including reading data from the models, then generates and returns an HTML page (from a template, into which we pass a context containing the data to be displayed).
What makes things more complicated is that the server also needs to be able to process data provided by the user, and redisplay the page if there are any errors.

![flowchart of how Django handles form requests](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms/form_handling_-_standard.png)

### Renew something form using a Form and function view

> Form

The Form class is the heart of Django's form handling system. It specifies the fields in the form, their layout, display widgets, labels, initial values, valid values, and (once validated) the error messages associated with invalid fields. The class also provides methods for rendering itself in templates using predefined formats (tables, lists, etc.) or for getting the value of any element (enabling fine-grained manual rendering).

> Declaring a Form

The declaration syntax for a Form is very similar to that for declaring a Model, and shares the same field types (and some similar parameters).

Form data is stored in an application's forms.py file, inside the application directory.

> Form fields

The arguments that are common to most fields are listed below (these have sensible default values):
- required
- label
- label_suffix
- initial
- widget
- help_text
- error_messages
- validators
- localize
- disabled

> Validation

Django provides numerous places where you can validate your data. The easiest way to validate a single field is to override the method clean```_<fieldname>()``` for the field you want to check.

### ModelForms

If you’re building a database-driven app, chances are you’ll have forms that map closely to Django models.

> Field types

The generated Form class will have a form field for every model field specified, in the order specified in the fields attribute.

Each model field has a corresponding default form field. For example, a ***CharField*** on a model is represented as a ***CharField*** on a form. A model ***ManyToManyField*** is represented as a ***MultipleChoiceField***.




