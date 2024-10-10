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

git clone https://github.com/adarshsunil/mosquitto-mqtt-subscriber.git

cd mosquitto-mqtt-subscriber


Steps :

1. The Docker Compose file includes the images and ports for setting up Mosquitto Broker with default MQTT port : 1883 (docker-compose.yml)
2. Separate folders are created for config, log, and data  (mkdir -p mosquitto/config mosquitto/data mosquitto/log)
3. The configuration file mosquito.conf is inside config folder  to initialise the listener port, connections and log file
4. Start the Mosquitto-broker using docker-compose

	sudo docker-compose up -d
(-d flag is set to run the container in detached mode in background to free up the terminal


