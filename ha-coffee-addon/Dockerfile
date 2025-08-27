ARG BUILD_FROM=ghcr.io/home-assistant/amd64-base:3.19
FROM ${BUILD_FROM}

# Установим зависимости
RUN apk add --no-cache python3 py3-pip bluez dbus

# Копируем файлы аддона
COPY run.sh /
COPY requirements.txt /
COPY coffee_mqtt.py /

RUN pip3 install --no-cache-dir -r /requirements.txt

CMD [ "/run.sh" ]
