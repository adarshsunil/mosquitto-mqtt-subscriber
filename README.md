Task 1: Set up Mosquitto Broker Using Docker Compose
- Description: Set up the Mosquitto MQTT broker using Docker Compose. Ensure the broker is accessible on the default MQTT port (1883) and configure it to allow device connections.
- Requirements:
	- Mosquitto broker should be run as a service using Docker Compose.
	- The broker must be accessible from the device simulator.
	- Provide instructions on how to start and stop the Mosquitto broker using Docker Compose.

 Prerequisites
- [Docker](https://docs.docker.com/get-docker/) installed on your system.
- [Docker Compose](https://docs.docker.com/compose/install/) installed.


Clone this repository to your local machine:
```bash
git clone https://github.com/adarshsunil/mosquitto-mqtt-subscriber.git

cd mosquitto-mqtt-subscriber

```
The Docker Compose file includes the images and ports for setting up Mosquitto Broker with default MQTT port : 1883 (docker-compose.yml)

Separate folders are created for log, and data
```bash
mkdir -p mosquitto/data mosquitto/log
```
The configuration file mosquito.conf is inside config folder  to initialise the listener port, connections and log file

Start the Mosquitto-broker using docker-compose

```bash
sudo docker-compose up -d
```

(-d flag is set to run the container in detached mode in background to free up the terminal

Testing publish and subscribe with Mosquitto. 

First subscribe to a particular topic (Here ‘test/topic’) with mosquitto_sub. 
```bash
mosquitto_sub -h localhost -p 1883 -t "test/topic"
```


Publish the content under the same topic from other terminal using mosquitto_pub
```bash
mosquitto_pub -h localhost -p 1883 -t "test/topic" -m "Hello, PowerPal at Maynooth"
```


Log file of Mosquitto will be available at mosquitto/log. This file can be viewed from the command prompt by :

```bash
 sudo cat mosquitto/log/mosquitto.log
```
To stop Docker, use
```bash
docker-compose down
'''

