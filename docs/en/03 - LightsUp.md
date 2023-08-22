# LightsUp!

# Pre-requisites to Get Started

1. Install flutter - [https://docs.flutter.dev/get-started/install](https://docs.flutter.dev/get-started/install)
2. Setup your IDE - [https://docs.flutter.dev/get-started/editor?tab=vscode](https://docs.flutter.dev/get-started/editor?tab=vscode)
3. Test drive - [https://docs.flutter.dev/get-started/test-drive?tab=vscode](https://docs.flutter.dev/get-started/test-drive?tab=vscode)
4. Writing your first app - [https://codelabs.developers.google.com/codelabs/flutter-codelab-first#0](https://codelabs.developers.google.com/codelabs/flutter-codelab-first#0)

# Resources to Keep Going

1. Dart Programming Language - [https://dart.dev/language](https://dart.dev/language)
2. Dart cheatsheet codelab - [https://dart.dev/codelabs/dart-cheatsheet](https://dart.dev/codelabs/dart-cheatsheet)
3. Riverpod - [https://codewithandrea.com/articles/flutter-state-management-riverpod/](https://codewithandrea.com/articles/flutter-state-management-riverpod/)

# Objectives

We are going to create a mobile app that runs in Android and iOS to showcase the various MQTT concepts we've learned in the previous chapters and expand more on other MQTT features.

The app showcases the following features:

- Dynamic creation of authenticated MQTT client connections to enhance security
- Ability to control the built-in LED light of an ESP8266 NodeMCU by turning it on / off
- One client controls the light and another can listen in realtime whether the light is on or not
- Realtime handling of MQTT messages shown in both the mobile app and ESP8266 LED

# Where do I start?

A GitHub repository is setup as easy starting point that has all the codes required to build the frontend. Since our focus is on MQTT communication, we will go through it together in this chapter.

Clone this git repo and checkout or download the `start/lights-up` branch.

[https://github.com/ahdzlee/iPBL2023-PreTraining/tree/start/lights-up/mobile/lights_up](https://github.com/ahdzlee/iPBL2023-PreTraining/tree/start/lights-up/mobile/lights_up)

# Video Lessons

Hands-on video sessions are created to get the app running and get the objectives covered. Please see the links below in the order as suggested.

1. [Intro and Project Structure](https://youtu.be/FbndnKULc8E)
   - Shows the relevant project files you need to be aware of and how to run the project in Visual Studio Code.
1. [Creating the MQTT Client Manager](https://youtu.be/Xg-AAr1IL2E)
   - Implements the class that handles client connection, disconnection, subscription, and publishing of MQTT messages. The manager also exposes a stream to listen for subscription updates.
1. [Creating an MQTT Client Connection](https://youtu.be/2Yv1fI4ulR8)
   - Shows how to use the MQTT Client Manager to create client connections to the broker.
1. [Keeping track of app connection state changes with Riverpod](https://youtu.be/mP_LQKsqJj0)
   - Shows how to use riverpod to manage app state changes. The app connection lifecycle changes are shown and how to get the user interface to update on state changes.
1. [Creating authenticated client connections](https://youtu.be/eVuhqOFzBeU)
   - Demonstrates how to activate authentication by accepting credentials in the broker. The app also handles the unauthorized exception and not let it create the client connection.
1. [Publishing events to turn lights on/off](https://youtu.be/3-4AGUBcNqU)
   - Sending payloads to the broker and testing it via MQTTX
1. [Subscribing to MQTT topics](https://youtu.be/mUgx4FV6ovY)
   - Shows how to subscribe to an MQTT topic and continuously listen for received MQTT message subscribed.
1. [Publish-Subscribe implementation in ESP8266 NodeMCU](https://youtu.be/pBd3tbD6LB8)
   - Create a sketch to flash to ESP8266 to handle builtin LED being turned on or off.

Thanks and have fun!
