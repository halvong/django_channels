Django2 & Channels 2, Apress Book
10/02/2019, Wed 

chp2, pg28


#steps
1. docker-compose exec web python manage.py startapp main 

#path
/home/hal/Documents/softwares/pro-pycharm/workspace/django/django-channels/django_channels



#notes
docker-compose up --build
docker-compose up -d database 
docker-compose logs database 
docker-compose build web 
docker-compose up -d web 
docker-compose logs -f web 
docker-compose exec web python manage.py makemigrations books
docker-compose exec web python manage.py sqlmigrate books 0001 
docker-compose exec web python manage.py migrate
docker-compose run --rm database psql -U tom -h database
		password: tom
docker-compose exec web python manage.py createsuperuser
docker-compose exec web python manage.py shell
docker-compose up -d --force-recreate web  
