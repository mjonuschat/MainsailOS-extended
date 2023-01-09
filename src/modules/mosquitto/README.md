# Mosquitto MQTT Server

CustomPiOS module to enable the Mosquitto MQTT server on startup.

## Secure the Mosquitto Server

The default configuration of Mosquitto allows for unauthenticated client
connections from anywhere. To secure the server connections provide a username
and password in `conf.local` according to the following example:

```sh
MOSQUITTO_USERNAME="myuser"
MOSQUITTO_PASSWORD="mypassword"
```
