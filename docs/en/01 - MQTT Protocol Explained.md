# MQTT Protocol Explained

# What is MQTT

MQTT stands for Message Queuing Telemetry Transport. It is a messaging protocol created for easy and efficient communication between devices in an IoT (Internet of Things) environment.

The MQTT protocol uses a publish-subscribe model for efficient data transmission by allowing devices to publish messages to specific topics and other devices to subscribe to those topics to receive the messages. This reduces network bandwidth usage.

Some key features of MQTT include:

1. Lightweight: MQTT is designed to be a lightweight protocol, making it suitable for constrained devices with limited processing power and bandwidth.
2. Asynchronous communication: MQTT allows devices to send and receive messages asynchronously, enabling efficient communication even in unreliable network conditions.
3. MQTT has three levels of Quality of Service (QoS) which determine how reliably messages are delivered. These levels are QoS 0, QoS 1, and QoS 2.
   - QoS 0 (At most once)
   - QoS 1 (At least once)
   - QoS 2 (Exactly once)
4. Scalability: MQTT is highly scalable and can support a large number of devices and subscribers, making it ideal for IoT deployments.
5. Efficient network usage: MQTT uses a compact binary message format, which helps to minimize network bandwidth usage.

MQTT has gained popularity in the IoT industry due to its simplicity, efficiency, and ability to work with a wide range of devices and platforms. It is widely used in applications such as home automation, industrial monitoring, and telematics, where efficient and reliable communication is essential.

# How does MQTT Work

To understand how MQTT works, you need to master the following basic concepts:

## MQTT Client

- Any app or device running an MQTT client library is an MQTT client. For example, a chat messaging app that uses MQTT is a client, sensors that use MQTT to report data are a client, and MQTT testing tools are also a client.

## MQTT Broker

- The broker handles connection, disconnection, subscription, and unsubscription requests and routing of messages.

## Publish-Subscribe Pattern

- As the name suggests, it is a pattern for sending and receiving MQTT messages. Publishers and subscribers do not need to establish a direct connection as the MQTT Broker is responsible for routing and distributing all messages.
- The diagram below shows the MQTT publish/subscribe process. The temperature sensor connectes to the MQTT server as a client and publishes temperature data to a topic (e.g., `temp`), and the server receives the message and forwards it to all clients that subscribed to `temp` topic.

![pub-sub.png](../assets/pub-sub.png)

## Topic

The MQTT protocol uses topics to route messages, and these topics are organized in a hierarchy using slashes (`/`), similar to URL paths. For example,

- `chat/room/1`
- `sensor/10/temperature`
- `sensor/+/temperature`

MQTT topic support the following wildcards: `+` and `#`

- `+` indicates a single level of wildcards, such as `a/+` matching `a/x` or `a/y`.
- `#` indicates multiple levels of wildcards, such as `a/#` matching `a/x`, `a/b/c/d`.

For more details on MQTT topics, please check the blog [Understanding MQTT Topics & Wildcards by Case](https://www.emqx.com/en/blog/advanced-features-of-mqtt-topics).

## **Quality of Service (QoS)**

MQTT provides three kinds of Quality of Service and guarantees messaging reliability in different network environments.

- QoS 0: The message is delivered at most once. If the client is not available currently, it will lose this message.
- QoS 1: The message is delivered at least once. High chance of message duplication.
- QoS 2: The message is delivered only once.

For more details on MQTT QoS, please check the blog [Introduction to MQTT QoS (Quality of Service)](https://www.emqx.com/en/blog/introduction-to-mqtt-qos).

# The MQTT Workflow

Now that we understand the basic components of MQTT, let's see how the general workflow works:

1. **Clients initiate a connection** to the broker using TCP/IP, with optional TLS/SSL encryption for secure communication. Clients provide authentication credentials and specify a clean or persistent session.
2. **Clients either publish messages to specific topics or subscribe to topics** to receive messages. Publishing clients send messages to the broker, while subscribing clients express interest in receiving messages on particular topics.
3. **The broker receives published messages** and forwards them to all clients subscribed to the relevant topics. It ensures reliable message delivery according to the specified Quality of Service (QoS) level and manages message storage for disconnected clients based on session type.
