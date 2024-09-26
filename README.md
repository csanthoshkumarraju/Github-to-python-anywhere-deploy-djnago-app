# Github-to-python-anywhere-deploy-djnago-app

Youtube link - https://youtu.be/lpw8J6EuPGU?si=51684YQzScyOYvig

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




----*******************-----

Guide: Uploading a Django Project from GitHub to PythonAnywhere

Preparation
1. Freeze Requirements: In your local Django project directory, run: pip freeze > requirements.txt.

Upload Project to GitHub
1. Initialize Git Repository: git init.
2. Add and Commit Changes: 
   git add .
   git commit -m "Initial commit".
3. Push to GitHub: 
   git remote add origin <your-github-repo-URL>
   git push -u origin master.

Set Up on PythonAnywhere
1. Log in to PythonAnywhere.
2. Open a Bash Console: Navigate to the Consoles tab and start a new Bash console.
3. Clone Your Repository: 
   git clone <your-github-repo-URL>
   cd <repository-name>.
4. Verify Current Directory: Use pwd.

Configure Your Project
1. Create a Virtual Environment: python -m venv virtualenv.
2. Activate the Virtual Environment: source virtualenv/bin/activate.
3. Install Dependencies: pip install -r requirements.txt.

Configure Your Web App
1. Create a New Web App: Go to the Web tab, click Add a new web app, choose Manual configuration, select Python 3.10.
2. Update settings.py: Set DEBUG = False and add paths for:
   - Main project directory: /home/username/<your-repo>
   - Project folder: (where manage.py is located)
   - Virtual environment: /home/username/<your-repo>/virtualenv
   - Static files directory: /home/username/<your-repo>/static
   - Media directory: /home/username/<your-repo>/media.
3. Configure WSGI: Click the WSGI link in the Web tab and update the WSGI file:
   import sys
   import os

   path = '/home/username/<your-repo>'
   if path not in sys.path:
       sys.path.append(path)

   os.environ['DJANGO_SETTINGS_MODULE'] = '<your_project>.settings'

   from django.core.wsgi import get_wsgi_application
   application = get_wsgi_application().

Collect Static Files
Run: python manage.py collectstatic.

Final Steps
1. Reload Your Web App: Go to the Web tab and click Reload.
2. Access Your Site: Visit your PythonAnywhere domain.

Troubleshooting
- Check error logs in the Web tab.
- Verify paths in settings.py.
- Confirm dependencies in requirements.txt.

