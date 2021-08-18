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
>