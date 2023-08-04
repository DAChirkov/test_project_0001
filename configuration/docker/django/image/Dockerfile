FROM python:3

WORKDIR /usr/src/app/project0001

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . /usr/src/app

RUN python manage.py migrate
CMD python manage.py runserver 0.0.0.0:8000