FROM python:3.9.10-slim

WORKDIR /app
COPY . /app
RUN pip install -r requirements.txt
EXPOSE 8000

CMD gunicorn --statsd-host=statsd-exporter:9125 --statsd-prefix=${APP_NAME} --bind=0.0.0.0:8000 app:app
