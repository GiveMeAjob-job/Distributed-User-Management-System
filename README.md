## Milestone Design

### **Phase 1: Project Initialization and Core Feature Development**
**Goal:** Complete the basic functionality of the system, ensuring that user registration, login, role management, and access control are operational in the local environment.

- [ ] **Milestone 1.1: Set up Spring Boot Project**
  - Set up the basic Spring Boot project structure
  - Integrate key dependencies such as Spring Web, Spring Data JPA, Spring Security
  - Configure database connections (MySQL or PostgreSQL)

- [ ] **Milestone 1.2: User Registration and Login Functionality**
  - Implement user registration and login functionality, using BCrypt to encrypt stored passwords
  - Configure JWT (JSON Web Token) for authentication

- [ ] **Milestone 1.3: Role and Permission Management**
  - Implement role management (User, Admin)
  - Set up role-based access control (RBAC)

---

### **Phase 2: Microservice Decomposition and Containerization**
**Goal:** Decompose the existing monolithic application into multiple microservices and implement containerized deployment.

- [ ] **Milestone 2.1: Microservice Decomposition**
  - Decompose the existing user management module into independent microservices
  - Decouple the permission management, user management, and authentication modules

- [ ] **Milestone 2.2: Docker Containerization**
  - Package each microservice as a Docker container
  - Use Docker Compose to manage local startup of multiple microservices

- [ ] **Milestone 2.3: Inter-Service Communication and Security**
  - Implement secure communication between microservices
  - Ensure JWT is transmitted and validated across different services

---

### **Phase 3: Microservice Expansion and Spring Cloud Integration**
**Goal:** Integrate Spring Cloud components such as Eureka for service discovery and API Gateway for enhanced scalability, service discovery, and load balancing.

- [ ] **Milestone 3.1: Integrate Spring Cloud Eureka (Service Registration and Discovery)**
  - Introduce Eureka Server and Eureka Client
  - Enable service registration and discovery

- [ ] **Milestone 3.2: Integrate Spring Cloud Gateway (API Gateway)**
  - Introduce Spring Cloud Gateway as the API gateway
  - Configure rate limiting, load balancing, and security authentication (e.g., JWT validation)

- [ ] **Milestone 3.3: Integrate Spring Cloud Config (Configuration Center)**
  - Introduce Spring Cloud Config to centralize configuration management
  - Set up a Config Server and host configuration files

---

### **Phase 4: Kubernetes Deployment and Expansion**
**Goal:** Migrate microservices to the Kubernetes environment, enabling auto-scaling, load balancing, service recovery, and rolling updates.

- [ ] **Milestone 4.1: Deploy Microservices to Kubernetes**
  - Deploy Dockerized microservices to a Kubernetes cluster

- [ ] **Milestone 4.2: Implement Auto-Scaling and Load Balancing**
  - Configure Kubernetes Horizontal Pod Autoscaler (HPA)
  - Implement auto-scaling and load balancing of service instances

- [ ] **Milestone 4.3: Monitoring and Logging**
  - Introduce Prometheus and Grafana to monitor the cluster
  - Integrate ELK (Elasticsearch + Logstash + Kibana) for log collection and analysis

---

### **Milestone Summary**
1. **Phase 1**: Project initialization, completion of basic user management features, and role-based access control, tested locally.
2. **Phase 2**: Decompose the system into microservices and containerize them, preparing for distributed deployment.
3. **Phase 3**: Introduce Spring Cloud components to improve system scalability, manageability, and fault tolerance.
4. **Phase 4**: Deploy microservices to a Kubernetes cluster, achieving automatic scaling, service discovery, and monitoring under a distributed architecture.
