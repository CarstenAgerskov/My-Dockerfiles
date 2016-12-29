## OpenHAB2 Dockerfile

## Build

docker build -t carsten/openhab2 .

### Exposed ports

8080

## Container start

docker run -p 8080:8080 --dns 192.168.1.1 -t -i --name=openhab2 carsten/openhab2

## Test



