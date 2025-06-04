# EXPERIMENT-05-Data-Publishing-to-IoT-Broker-Using-MQTT3

## Aim:
To publish data to an IoT broker using the MQTT protocol.

## Apparatus Required:
MQTT Broker: An MQTT broker, such as HiveMQ or Mosquitto, for handling communication.
Python Environment: To run the script for publishing data to the broker.
Internet Connection: For connecting to the IoT broker.
Theory:
MQTT (Message Queuing Telemetry Transport) is a lightweight messaging protocol used in IoT applications. It allows devices to publish data to a broker, where other devices or applications can subscribe to receive updates. This experiment demonstrates how to use MQTT to send messages to an IoT broker using the paho-mqtt library in Python.

## Procedure:
Setup MQTT Broker:

-> You can use a public broker like broker.hivemq.com or set up your own broker using software like Mosquitto.
-> Choose a topic for the message, e.g., test/topic.
-> Install MQTT Client Library:
-> Install the paho-mqtt Python library to facilitate communication with the MQTT broker.
-> Write the Python Script to Publish Data:
-> Create a Python script to connect to the broker and publish a message to a specific topic.

## Python Code:
```
!pip install paho-mqtt
```
```
import paho.mqtt.client as mqtt
broker_address = "broker.hivemq.com"
broker_port = 1883
topic = "test/topic"

client = mqtt.Client()
client.connect(broker_address, broker_port, keepalive=60)
message = "hello MQTT"
client.publish(topic,message)
client.disconnect()
print(f"Message '{message}' published to topic '{topic}'")
```

## Outputs:
![image](https://github.com/user-attachments/assets/1d94cda8-a75e-4af3-8713-b3100d848b06)

![image](https://github.com/user-attachments/assets/c7ca1806-3ecc-45f3-8a41-f493cea9642f)

![image](https://github.com/user-attachments/assets/0936f26c-f4bc-46cd-8a82-c5d872118d5b)


## Results:
The data was successfully published to the MQTT broker. The experiment demonstrated how to use the MQTT protocol to transfer data to an IoT broker, enabling remote communication between devices or applications. The message was confirmed to be received by the topic, and this communication can be extended to more complex IoT systems.
