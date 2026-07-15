Project: LinkedIn Clone — Microservices-based Social Networking Platform

Tech Stack & Tools:
Java 21, Spring Boot 3.x, Maven, PostgreSQL, Neo4j, Apache Kafka, Spring Cloud Gateway, Netflix Eureka, OpenFeign, Docker, Kubernetes, Jib, Cloudinary, JWT, BCrypt

1.Architected and developed a LinkedIn-like social networking platform using a microservices architecture with 7 independent services (API Gateway, User Service, Posts Service, 
Connections Service, Notification Service, Uploader Service, Eureka Discovery Server) communicating via OpenFeign and Apache Kafka.

2.Implemented event-driven architecture using Apache Kafka for asynchronous communication, including user creation events triggering automatic Person node creation in Neo4j,
and post/like events generating persisted notifications.

3.Built a Spring Cloud Gateway with custom JWT authentication filter that validates tokens, extracts userId, and propagates it via X-User-Id header across all
downstream services.

4.Developed a graph-based social connections system using Neo4j with Cypher queries to manage connection requests (send/accept/reject) and retrieve first-degree
connections through bidirectional CONNECTED_TO relationships.

5.Implemented image upload functionality with Cloudinary CDN integration, with an alternative Google Cloud Storage implementation available.

6.Containerized all microservices using Jib Maven Plugin (zero-Dockerfile approach) and deployed to Kubernetes with comprehensive YAML manifests including 
StatefulSets for databases, Deployments for services, and Ingress routing.

7.Deployed a production-grade Kubernetes cluster with PostgreSQL StatefulSets (persistent volumes), Neo4j graph database, Kafka in KRaft mode (2 replicas), and
resource-constrained container specifications.

8.Implemented secure user authentication with BCrypt password hashing, JWT token generation/validation (HMAC-SHA), and stateless session management.

9.Designed a layered architecture with REST controllers, service layer, repositories, and DTOs, along with centralized exception handling via @RestControllerAdvice
across all services.

10.Built a real-time notification system via Kafka consumers that creates and persists database notifications when connections create posts or interact with content.



