# What is Django?
- Django is a back-end server side web framework.
- Django is free, open source and written in Python. 
- Django makes it easier to build web pages using Python.
- Django follows **MVC (model-view-controller)** architecture pattern, written in Python programming language and designed for creating easy apps with rapid development.

# Prerequisite to install virtual environment Django :
- Before learning Django, you must know the basics of Python coding.
- Gaining a thorough understanding of another coding language can make learning Python much easier.
- Two solid programming languages to start with are HTML and CSS
- To install Django, you must have Python installed
  
   To check if your system has Python installed, run this command in the command prompt :
   
  ```sh
  python --version
   ```
   If show the python version then it is ok
  
- Code editor for example : Vs code

# Setting up a virtual environment Django setup steps :

- To create a virtual environment for your project, open a new command prompt, navigate to the folder where you want to create your project and then enter the following command :

  ```sh
  python -m venv environment-project-name
  ```
  This will create a folder called `environment-project-name` if it does not already exist and set up the virtual environment. To activate the environment, run :

  ```sh
  . environment-project-name/Scripts/activate
  ```
  The virtual environment will be activated and you’ll see “(environment-project-name)” next to the command prompt to designate that.
  
  Now Django can be installed easily using pip within your virtual environment.
  
  In the command prompt, ensure your virtual environment is active, and execute the following command :

  ```sh
  pip install django
  ```
  This will download and install the latest Django release.

  Now we will create the main project folder `project-name` where we can easily all coding work so follow the command :

  ```sh
  django-admin startproject project-name
  ```
  This will create a folder called `project-name` if it does not already exist and set up the project folder.
  
  Now we will create app inside the `main project folder` so follow the command  to access the right path folder :
  
  ```sh
  cd project-name/
  ```
  Now we will create the app folder so follow the command :

  ```sh
  python manage.py startapp app-name
  ```

  Now we will app folder `app-name` connect the created main project folder `project-name`

  First go to main project `project-name` folder and select the `settings.py` and accress the file and go to the `INSTALLED_APPS` section look like

  ```sh
  # Application definition

  INSTALLED_APPS = [
  	'django.contrib.admin',
  	'django.contrib.auth',
  	'django.contrib.contenttypes',
  	'django.contrib.sessions',
  	'django.contrib.messages',
  	'django.contrib.staticfiles',
  ]

  ```
  
  Now add my app folder `app-name` after add app folder now look like

	 ```sh
	# Application definition
			
	INSTALLED_APPS = [
		'django.contrib.admin',
		'django.contrib.auth',
		'django.contrib.contenttypes',
		'django.contrib.sessions',
		'django.contrib.messages',
		'django.contrib.staticfiles',
		'app-name',
	]
	 ```
  
   Now app folder connection is `OK`

   Now we will run the project so follow the command :

   ```sh
   python manage.py runserver
   ```
   Which will produce this result look like :

  ```sh
  Watching for file changes with StatReloader
  Performing system checks...

  System check identified no issues (0 silenced).

  You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
  Run 'python manage.py migrate' to apply them.
  October 27, 2022 - 13:03:14
  Django version 4.1.2, using settings 'project-name.settings'
  Starting development server at http://127.0.0.1:8000/
  Quit the server with CTRL-BREAK.
  ```

  Open a new browser window and type 127.0.0.1:8000 in the address bar. The result look like :
  
  ![Preview Result of Successfully Installation is Done of Django](https://www.w3schools.com/django/screenshot_django1.png)

  Now Installation is `Done`



  Now if i will want to make custom html file and work this file then we would follow the some step :

  Go to create main project folder `project-name` and select the file `urls.py` now modify some code look like bellow :

  Need some code copy fast to use after

  ```sh
	  from django.urls import path
	
	urlpatterns = [
	    path('admin/', admin.site.urls),
	]

  ```

  
   









