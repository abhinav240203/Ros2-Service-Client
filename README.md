# ROS2 Service Client–Server

A ROS 2 project demonstrating a simple service-based communication system where a client sends two integers to a server and receives their sum as a response. This project is designed to 
understand ROS 2 service creation, request-response communication, and node interaction.

---

## 🚀 Features

* Custom ROS2 service (`AddTwoInts`)
* Request-response communication between nodes
* Service server handling incoming requests
* Service client sending requests and receiving responses
* Logging of request and response data

---

## 📋 Service Definition

```
# Request
int64 a
int64 b
---
# Response
int64 sum
```

The service takes two integers as input and returns their sum as output.

---

## 🤖 Service Server Behavior

The service server creates and advertises the `add_two_ints` service. It continuously waits for incoming requests from clients. When a request is received, it extracts the two integer values,
computes their sum, and sends the result back to the client. It also logs the received inputs and the computed result for verification.

---

## 💻 Service Client Behavior

The service client connects to the `add_two_ints` service and sends a request containing two integers. It waits until the service becomes available, sends the request, and then
waits for the response. Once the response is received, it prints the computed sum.

---

## 🔄 Communication Flow

1. Service server starts and waits for requests
2. Client sends two integers
3. Server receives request
4. Server computes sum
5. Server sends response
6. Client receives and displays result

---

## 🎯 Learning Outcome

This project demonstrates how ROS2 services work in practice, including request-response communication, service creation, client-server interaction, 
and basic distributed node communication in robotics systems.
