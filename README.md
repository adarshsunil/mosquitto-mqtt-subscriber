Task 1: Set up Mosquitto Broker Using Docker Compose
- Description: Set up the Mosquitto MQTT broker using Docker Compose. Ensure the broker is accessible on the default MQTT port (1883) and configure it to allow device connections.
- Requirements:
	- Mosquitto broker should be run as a service using Docker Compose.
	- The broker must be accessible from the device simulator.
	- Provide instructions on how to start and stop the Mosquitto broker using Docker Compose.

Steps :

1. Create the Docker Compose file for setting up Mosquitto Broker with default MQTT port : 1883 (docker-compose.yml)
2. Separate folders are created for config, log, and data  (mkdir -p mosquitto/config mosquitto/data mosquitto/log)
