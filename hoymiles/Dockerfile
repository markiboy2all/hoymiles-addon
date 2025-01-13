ARG BUILD_FROM
FROM $BUILD_FROM

# Install requirements for add-on
RUN \
  apk add --no-cache \
    python3

# Python 3 HTTP Server serves the current working dir
# So let's set it to our add-on persistent data directory.
WORKDIR /hoymiles-mqtt

COPY . .
RUN pip3 install -e .

CMD [ "python3", "-m" , "hoymiles_mqtt"]