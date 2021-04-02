# Waryongs-Server

## Getting Started


### Set up Python virtual environment and build apps
$python -m venv waryongs    
$C:\venvs\waryongs\Scrips\activate    
$pip install django==3.1.3    
$pip install djangorestframework    
$django-admin startproject config .    


    
### Clone project
https://github.com/EJ719/Waryongs-Server.git    

cd into folder    
cd waryongs    


    
### Modify settings.py (waryongs/settings.py)
LANGUAGE_CODE = ‘ko-kr’    
TIME_ZONE = ‘Asia/Seoul’


    
### Database migrate
$python manage.py migrate


    
### Create Application
$python manage.py startapp waryongs
 
 
     
### Modify config/urls.py
    from django.urls import path
    from waryongs import views…
        path(‘admin/’, admin.site.urls),
        path(‘warongs/’ views.index),
    )
 
 
     
### Created waryongs/urls.py
    from django.conf.urls import url
    from waryongs import views

    urlpatterns=[
	    url(r’^$’, views.index, name=’index’),
    ]


    
### Add waryongs/views.py
    from django.http import HttpResponse
    
    def index(request:
        return HttpResponse(“안녕하세요. 와룡이들입니다.”)


    
### Run Web Server
$python manage.py runserver
