ARG BUILD_FROM=ghcr.io/home-assistant/aarch64-base:latest
FROM $BUILD_FROM

RUN apk add --no-cache python3 py3-pip bluez dbus

COPY run.sh /
COPY requirements.txt /
COPY coffee_mqtt.py /

RUN pip3 install --no-cache-dir --break-system-packages -r /requirements.txt

CMD [ "/run.sh" ]
