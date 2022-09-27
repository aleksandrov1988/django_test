* Создаём `requirements.txt` c содержимым `Django`

~~~~
echo "Django" > requirements.txt
python3 -m pip install --upgrade pip
pip install -r requirements.txt
django-admin startproject mysite .
~~~~

Правим часовой пояс и локаль

~~~~
python manage.py migrate
python manage.py runserver
python manage.py startapp blog
~~~~

* Добавляем `blog` в `settings.py` `INSTALLED_APPS`
* Создаём модель в `blog/models.py`

~~~~
python manage.py makemigrations blog
python manage.py migrate blog
python manage.py createsuperuser
~~~~

~~~~
git init
~~~~

### `.gitignore`

~~~~
*.pyc
*~
__pycache__
myvenv
db.sqlite3
/static
.DS_Store
~~~~
