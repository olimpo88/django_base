FROM python:2.7-stretch


RUN apt-get update && apt-get install libsasl2-dev python-dev libldap2-dev libssl-dev python-ldap libkf5ldap-dev xfonts-base xfonts-75dpi gettext -y --force-yes

WORKDIR /usr/src/app

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 8000


RUN mkdir /script 
COPY runserver.sh /script
COPY wait-for-it.sh /script
RUN chmod +x /script -R

CMD ["/script/wait-for-it.sh", "postgres:5432", "--", "/script/runserver.sh"]
#CMD ["python","manage.py","runserver","0.0.0.0:8000"]
