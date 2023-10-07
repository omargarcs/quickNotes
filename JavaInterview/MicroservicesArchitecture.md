Microservices architecture is an approach to building software systems where applications are composed of loosely coupled, independently deployable services. Each service in a microservices architecture typically focuses on a specific business capability, and these services communicate with each other over well-defined APIs. When designing microservices, there are several patterns that can help you create scalable, maintainable, and resilient systems. Here are some important microservices design patterns:

1. **Service Decomposition**: Breaking down the application into smaller, focused services is the foundational principle of microservices. Identify the bounded contexts within your application and decompose them into individual services. Each service should have a clear responsibility.

2. **API Gateway**: An API gateway acts as a single entry point for client applications to interact with the microservices. It can handle tasks such as authentication, load balancing, and routing requests to the appropriate services. This pattern helps manage the complexity of client interactions.

3. **Service Registry and Discovery**: In a dynamic microservices environment, services may come and go. A service registry allows services to register themselves, and a discovery mechanism allows other services to locate and communicate with them. Tools like Netflix Eureka can be used for this purpose.

4. **Load Balancing**: Distribute incoming requests evenly across instances of a service to improve performance and ensure high availability. Load balancing can be performed at the client side or by using dedicated load balancers.

5. **Database per Service**: Each microservice should have its own dedicated database, ensuring data isolation and making it easier to manage and scale individual services. Implementing this pattern may require careful consideration of data consistency.

6. **Event Sourcing**: In event sourcing, the state of the application is determined by a sequence of events, which are stored and can be replayed. This pattern is useful for maintaining a history of changes, auditing, and building complex workflows.

7. **Circuit Breaker**: Implement a circuit breaker pattern to prevent cascading failures when a service dependency is unavailable. The circuit breaker can temporarily "open" to stop sending requests to a failing service and "close" when the service is healthy again.

8. **Asynchronous Communication**: Use message queues or publish-subscribe systems for asynchronous communication between services. This pattern helps decouple services and handle peak loads without blocking.

9. **Authentication and Authorization**: Implement security measures at both the microservice level and the API gateway level. Use mechanisms like OAuth2 for authorization and authentication.

10. **Monitoring and Logging**: Implement comprehensive monitoring and logging for each service to track performance, identify issues, and ensure the overall health of the system.

11. **Polyglot Persistence**: Choose the most suitable database technology for each service's data needs. Different services may use different types of databases (relational, NoSQL, etc.).

12. **Containerization**: Consider using containers (e.g., Docker) for packaging and deploying microservices. Containerization simplifies deployment and ensures consistent environments.

Remember that the choice and combination of these patterns should be based on the specific requirements of your application, the technology stack you're using, and the challenges you're trying to address. Also, keep in mind that adopting microservices comes with operational complexities, and it's essential to have a solid DevOps strategy in place to manage the deployment, scaling, and monitoring of your microservices.