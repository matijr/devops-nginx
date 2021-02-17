FROM python:3.7-slim-buster
WORKDIR /backend
ENV SECRET_KEY=os.environ.setdefault
ENV DJANGO_SETTINGS_MODULE=backend.settings
#dependencias y librerias necesarias
RUN apt-get update -y 
RUN pip3 install --upgrade pip
RUN apt-get install gcc -y libpq-dev -y python3-dev -y libgraphviz-dev -y 
RUN pip3 install psycopg2-binary
COPY requirements.txt requirements.txt
#Instalacion de requisitos
RUN pip3 install -r requirements.txt
EXPOSE 4000
COPY . .
CMD [ "python3", "manage.py", "runserver", "0.0.0.0:4000" ]
