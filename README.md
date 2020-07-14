# SOFT-IoT Aplication

SOFT-IoT platform composes of a set of features that enable the implementation of Microservices for the construction of IoT applications. SOFT-IoT allows to create the following computational architectures: only networks of personal area sensors; personal area sensor network combined with gateway management, thus creating a local area network; network of personal area sensors with gateways and servers, thus creating a more robust local area network infrastructure; only Cloud Servers managing local devices; deployment of all infrastructure from the global network to the personal area network. Thus, the SOFT-IoT architecture is flexible and configurable to meet specific or generic infrastructure and application requirements.


## SOFT-IoT Microservices


### soft-iot-mapping-devices
This module is responsible for mapping devices connected with each FoT-Gateway. It is used by other modules to get access of basic information about devices and yours sensors/actuators.

link: https://github.com/WiserUFBA/soft-iot-mapping-devices

### soft-iot-local-storage
This module is responsible to collect data from sensors (using the configuration of fot-gateway-mapping-devices) and store them in a local database (Apache H2). For this, it uses a MQTT client (Paho) to get data from sensors and write this in the database.

link: https://github.com/WiserUFBA/soft-iot-local-storage

### soft-iot-local-storage
The microservice exposes sensor data of IoT system through a RESTful Web Service. It accesses data stored in local database, managed by soft-iot-local-storage, allowing users get data and information about sensors in JSON format.

link: https://github.com/WiserUFBA/soft-iot-iot-service

### soft-iot-auto-irrigation
The service collects weather data sensors using [fot-gateway-local-storage](https://github.com/WiserUFBA/fot-gateway-local-storage) and calculates the quantity of water to irrigate the crop.

link: https://github.com/leandrojsa/soft-iot-auto-irrigation
