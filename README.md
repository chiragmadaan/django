# django

django-admin startproject <proj_name>
ls proj_name
create database next to manage.py
python manage.py migrate
python manage.py createsuperuser
python manage.py startapp sales
python manage.py startapp reports
python manage.py startapp profiles
python manage.py startapp products
python manage.py startapp customers

python manage.py runserver
url/admin to view admin portal

pip install pillow django-crispy-formsmatplotlib seaborn pandas xhtml2pdf
pip freeze > requirements.txt
to install these packages in another venv/project: pip install -r requirements.txt

In proj_name/proj_name/settings.py
	extend INSTALLED_APPS list with stared apps
	Templates > Dirs: [BASE_DIR / 'templates']
	under STATIC_URL add STATICFILES_DIRS list, add BASE_DIR / 'static'
	add MEDIA_URL = '/media/
	add MEDIA_ROOT = BASE_DIR / 'media'

Create templates folder at same level as manage.py
Create base.html and navbar.html in templates folder

Create static folder at same level as manage.py
Create style.css in static

Create media folder at same level as manage.py

In proj_name/proj_name/urls.py
	edit import django.urls import path, include
	add import django.conf import settings
	add import django.conf.urls.static import static
	at bottom
	url_patterns += static(settings.STATIC_URL, document_root=settings.STATIC_ROOT)
	url_patterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)

Copy base.html code from https://blog.pyplane.com/blog/django-report-app/