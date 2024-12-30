# Django-Bugs-Errors---Solutions

<h3>Solution to problem 1:</h3>
The solution to this issue for me is detailed here: <a href="https://docs.djangoproject.com/en/4.2/howto/static-files/#serving-static-files-during-development"> Serving static files during development</a>

<h3>Just add this to your project's urls.py:</h3>
<code><br>
from django.conf import settings
from django.conf.urls.static import static
urlpatterns = [… the rest of your URLconf goes here …] + static(settings.STATIC_URL, document_root=settings.STATIC_ROOT)
<br></code>
