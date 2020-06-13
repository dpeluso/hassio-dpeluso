ARG BUILD_FROM
FROM $BUILD_FROM
RUN apk add python3

LABEL maintainer="tomer.klein@gmail.com"

ENV PYTHONIOENCODING=utf-8

RUN pip3 install --upgrade pip
RUN pip3 install flask flask_restful cryptography==2.6.1 broadlink --no-cache-dir

#Create working directory
RUN mkdir /opt/broadlinkmanager

EXPOSE 7020

COPY broadlinkmanager /opt/broadlinkmanager

ENTRYPOINT ["python3", "/opt/broadlinkmanager/broadlinkmanager.py"]
