FROM python:3
WORKDIR /usr/src/app
COPY requirements.txt ./
ENV HTTPS_PROXY=http://142.117.128.41:80/
ENV HTTP_PROXY=http://142.117.128.41:80/
RUN pip install -r requirements.txt
COPY . .
EXPOSE 8080
CMD [ "gunicorn", "--bind", "0.0.0.0:8080","wsgi:app" ]
