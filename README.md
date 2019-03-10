# ready4Heroku
Barebones where you can copy and ready to deploy to heroku.

don't need to worry about the collectstatic erros as that has been setup for you already.

You might want ot change the follwing to reference your specific project name as I would imagin you probrably don't want to call it ready4heroku

inside the directory: ready4heroku 

	settings.py
		ROOT_URLCONF = 'ready4heroku.urls'
		INSTALLED_APPS = [  ... blah...
		WSGI_APPLICATION = 'ready4heroku.wsgi.application'

	url.py 
		urlpatterns
		
	wsgi.py
		os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'ready4heroku.settings')

inside the directory: yourFirstApp
	urls.py
		urlpatterns
