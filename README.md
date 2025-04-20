## Spring Cloud Stream & Azure Servicebus Emulator - Consumer Example

### Prerequisites
- Docker
- docker-compose
- SCS-Sender (Spring Cloud Stream & Azure Servicebus Emulator Producer Example)
  - https://github.com/afsinka/servicebus-scs-sender

### Setup
- Run this SCS-Receiver application in your IDE
- It will start to listen the queue called "queue.1" in "sbemulatorns" namespace in "servicebus" as it is stated in "application.properties"
- After you send a request in SCS-Sender application with calling its Hello API e.g.
```
curl localhost:8081/hello/John
```
and if "servicebus emulator" also is running in Docker in your local setup then you will see SCS-Receiver application will receive a message and prints it in terminal e.g.
```
Incoming message GenericMessage [payload=Hello from John, headers={azure_service_bus_expires_at=2025-04-20T21:30:43.286Z...]
```

### References
- https://learn.microsoft.com/en-us/azure/service-bus-messaging/test-locally-with-service-bus-emulator?tabs=docker-linux-container
- https://learn.microsoft.com/en-us/azure/developer/java/spring-framework/developer-guide-overview#spring-cloud-stream-binder-for-azure-service-bus


