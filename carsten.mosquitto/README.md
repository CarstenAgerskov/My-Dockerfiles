## Mosquitto MQTT broker Dockerfile

## Build

docker build -t carsten/mosquitto .

### Exposed ports

tcp/1883  MQTT port  
tcp/9001  websocket

## Container start

Run for MQTT only:  
docker run -d -p 1883:1883 --name=mosquitto carsten/mosquitto

Run for MQTT + websocket:  
docker run -d -p 1883:1883 -p 9001:9001 --name=mosquitto carsten/mosquitto

## Test

mosquitto_sub -h localhost -v -t test/topic
then open another terminal and
mosquitto_pub -h localhost -t test/topic -m "Hello world from Mosquitto"

