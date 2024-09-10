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
- Git (optional)

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

  ```python
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

	 ```python
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

  Need some code copy fast to use after this step it is enough

  ```python
	  from django.urls import path
	
	urlpatterns = [
	    path('admin/', admin.site.urls),
	]
  ```

  Now modify `urls.py` this file look like bellow :

   Before modify this `urls.py` file code

   ```python
	from django.contrib import admin
	from django.urls import path
	
	urlpatterns = [
	    path('admin/', admin.site.urls),
	]
   ```
   
   After modify this `urls.py` file code

   ```python
	from django.contrib import admin
	from django.urls import path, include
	
	urlpatterns = [
	    path('admin/', admin.site.urls),
	    path('', include('app-name.urls'))
	]
   ```
  
   Now go to created `app-name` app folder and create the file `urls.py` inside this folder and paste the previously copy code look like bellow :

    ```python
	from django.urls import path
	
	urlpatterns = [
	   
 	]
    ```
   Now we will create the `templates` folder inside the created app `app-name` folder.

   Now create the `index.html` file inside the `templates` folder.

   Now right some code inside `html` file as your wish.

   Now if we want run the `index.html` file and if we want see the live server then follow some setup .

   Now select the app folder `app-name` and select inside the folder file `views.py` and
   we will make user defined function in this file look like bellow :

   ```python
     # Create your views here.

     def home(request):
     return render(request, "index.html")
    ```

    Now need call the function so go to the app folder `app-name` and select the file `urls.py` and write the code bellow :

    ```python
	from django.urls import path
	from . views import home
	
	urlpatterns = [
	    path('', home,name='index')
	]
    ```
  
    Now again run the project using command `python manage.py runserver` and see the output. `Done`


# Re-open the created Django project guide :

- First open the project folder by vs code
- Then open the termenal and write the code to active the Django environment

  ```sh
  . myenv/Scripts/activate
  ```
- Then move the project folder so follow the command

  ```sj
  cd myproject/
  ```
- Now run the project follow the command

  ```sh
  python manage.py runserver
  ```
- Done this work. `Done`

# Add custom template in Django guide :

- First download or create the template.
- Now template main index.html file move the django template folder drag and drop.
- The cerate the folder name `static` inside the `myapp` folder.
- Now go to the index.html file and all the `href` and `src` link tag modify the like this bellow :

  ```sh
  <link href="{% static 'asset/css/bootstrap.min.css' %}" rel="stylesheet">
  ```
  after done all of the link convert to static then follow the next step. Same procedure of the image tag also.

- Now write this code inside the top of `head` tag

  ```sh
  {% load static %}
  ```
- Now go to terminal runnig server stop to click `Ctrl + c` then stop the running server and again write the code

  ```sh
  python manage.py collectstatic
  ```
  after run the code and write the permission the terminal `yes` and continue
  
- Then go to the myproject folder and open the file `settings.py` and write the code

  find same type location 
  ```sh
  # Static files (CSS, JavaScript, Images)
  # https://docs.djangoproject.com/en/4.2/howto/static-files/

  STATIC_URL = 'static/'

  # Default primary key field type
  # https://docs.djangoproject.com/en/4.2/ref/settings/#default-auto-field
  ```

  after write code then show like bellow
  ```sh
  # Static files (CSS, JavaScript, Images)
  # https://docs.djangoproject.com/en/4.2/howto/static-files/

  STATIC_ROOT = BASE_DIR / 'static/' 
  STATIC_URL = 'static/'

  # Default primary key field type
  # https://docs.djangoproject.com/en/4.2/ref/settings/#default-auto-field

  DEFAULT_AUTO_FIELD = 'django.db.models.BigAutoField'
  ```
  
- Again write the code

  ```sh
  python manage.py collectstatic
  ```
- Now the code and run the project

  ```sh
  python manage.py runserver
  ```

- Now this work is done. `Done`



# Upload Image Backend and show template in Django guide :

First install the package
```sh
python -m pip install Pillow
```

Then `models.py` file for `image` code look like
```py
class Testimonial(models.Model):
    t_discription = models.CharField(max_length=250)
    name = models.CharField(max_length=80)
    t_designation = models.CharField(max_length=100)
    image= models.ImageField(upload_to='static/assets/img/testimonials/', default='#')
    
    def __str__(self):
     return self.name
```

Then `urls.py` file code look like

```py

from django.conf import settings
from django.conf.urls.static import static

urlpatterns = [

]

if settings.DEBUG:
    urlpatterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)

```
Then `settings.py` file and write the code look like

```sh
import os

MEDIA_URL = '/media/'
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
```















    
    
# Others Django command :

```sh
python manage.py makemigrations
```

```sh
python manage.py migrate
```

```sh
python manage.py createsuperuser
```



  

   

   






