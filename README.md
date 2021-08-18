# Django To-Do List
---
This is a basic to-do list for multiple users. It has full CRUD functionality, a search feature, and a little bit of styling.

As this was my first time using Django, I am going to include notes for myself (or really anyone reading this) about how things are structured and how it all comes together. Fair warning, this is simply me putting my understanding of this into words, and I am in no way infallible.

> From the root directory, we see two folders and four files. Of the four files, let's address `db.sqlite3` and `manage.py`. 
>
> **`db.sqlite3`** is a self-contained, serverless database engine. It allows us to store and retrieve information without actually setting up a server / database. This is given to use when we create a new django project.
>
> **`manage.py`** is also created for us when we create a new django project. It mainly does two things: 1) Points / Connects to the project's `settings.py` file. 2) Allows use to use `manage.py <...>` in the command line rather than `django-admin <...>` or `python -m django <...>`.
>> NOTE: Using `manage.py` for a command will only work if you are in the desired project's directory.
>
>
> Now let's look at the two folders; here they are named "base" and "DjangoToDo". The "DjangoToDo" folder is the **Project Folder**, and the "base" folder is an **App Folder**. There is only one project folder, but there can be many app folders. The files in the project folder exist / are used for the entire project, while each app folder contains everything needed for one particular aspect of the project. For example, if we think of Amazon, the cart and/or checkout process could be one app folder, while the list of products on the home page could be a seperate app folder.
>
> If we take a look inside the project folder, we see five files (all of which were given when we created the new django project): `_init_.py`, `asgi.py`, `settings.py`, `urls.py`, and `wsgi.py`.
>
> **`_init_.py`** is blank, and only exists to tell Python that this directory is a Python package.
>
> **`asgi.py`** and **`wsgi.py`** are entry points different web servers to serve the project.
>
> **`urls.py`** does what you expect based on its name, it holds all of the URL paths for the project. It is basically a table of contents.
>
> **`settings.py`** is also pretty straightforward about its purpose, it stores all of the settings / configurations for the project.

> Lastly, we have the app folder to discuss; however, currently I wish to improve my understanding before attempting to explain it. Within the next day or two, I will be adding comments throughout the code, and updating these README notes. This project was meant to be a learning experience, so I want to get the most out of it that I can.