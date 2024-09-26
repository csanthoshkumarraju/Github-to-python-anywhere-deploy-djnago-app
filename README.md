# Github-to-python-anywhere-deploy-djnago-app

pip freeze > requirements.txt  
Upload the Django project to GitHub.  
Copy the code HTTPS link.  
Open PythonAnywhere Bash.  
Run the PWD command.  
Git clone the copied HTTPS link.  
After 100% success in copying, from the right corner menu, open Files in a new tab.  
In the files, check the file name.  
In Bash, type `cd <file_name>`.  
Create a virtual environment:  
`python -m venv virtualenv`  
Reload the files page.  
We can see that the virtualenv virtual environment was created.  
Activate the virtual environment:  
`source virtualenv/bin/activate`  
Run `pip freeze > requirements.txt`.  
Copy all the requirements into requirements.txt in the files if they were not added before.  

Run `pip install -r requirements.txt`.  
Create a web app.  
Duplicate the PythonAnywhere files page.  
Click on "Web" and add a new web app.  
Click Next - Manual configuration - Python 3.10 - Next.  
Set up settings.py:  
Copy all the paths below and store them in Notepad:  
- Main project directory  
- Project folder  
- Virtual environment  
- Static files directory  
- Media directory  
Copy the templates and static files in settings.py and set `DEBUG = False`.  
Save.  
Set up the web app:  
- Source code path: Main project directory  
- Next, virtual environment path:  
Copy the URLs static path.  
Next, open the WSGI link in a new tab.  
Path = Main project directory.  
Next, for the settings path, paste the project folder.



---------------**********************-------------
https://youtu.be/lpw8J6EuPGU?si=51684YQzScyOYvig
