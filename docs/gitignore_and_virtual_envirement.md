# Working on this project in a virtual environment

In this file, we will address the important issue of how to run this project in a virtual environment.

You must use a virtual environment named **.venv**, which is created like this:

```cmd
python -m venv .venv
```

**This is very important!!!!** because only in this format will Git consider your virtual environment as project files and **never** push it to the repository on GitHub
The reason for this is the **large size of the virtual environment**, its personal nature, and the amortization of its movement with each pull and push.

Note that the contents of the data folder are not tracked by Git by default because they can also be large amounts of data.
If you need to move something specific, you can read the .gitignore file, which ignores items that are not important to Git, and modify it if necessary.