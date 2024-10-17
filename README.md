## 阶段性里程碑设计

### **阶段 1: 项目初始化与核心功能开发**
目标：完成系统的基础功能，确保用户注册、登录、角色管理和权限控制等核心功能能够在本地环境中运行。

- [ ] **里程碑 1.1: 搭建 Spring Boot 项目**
  - 搭建基础的 Spring Boot 项目结构
  - 集成基本依赖，如 Spring Web、Spring Data JPA、Spring Security
  - 配置数据库连接（MySQL 或 PostgreSQL）
  
- [ ] **里程碑 1.2: 用户注册与登录功能**
  - 实现用户注册和登录功能，使用 BCrypt 加密存储密码
  - 配置 JWT（JSON Web Token）用于身份认证
  
- [ ] **里程碑 1.3: 角色和权限管理**
  - 实现角色管理（用户、管理员）
  - 配置基于角色的访问控制（RBAC）

---

### **阶段 2: 微服务拆分与容器化**
目标：将现有的单体应用拆分为多个微服务，并实现容器化部署。

- [ ] **里程碑 2.1: 微服务拆分**
  - 将现有的用户管理模块拆分为独立的微服务
  - 将权限管理、用户管理、认证模块解耦

- [ ] **里程碑 2.2: Docker 容器化**
  - 将每个微服务打包成 Docker 容器
  - 使用 Docker Compose 管理多个微服务的本地启动

- [ ] **里程碑 2.3: 微服务间的通信与安全管理**
  - 实现微服务之间的通信安全管理
  - 确保 JWT 在不同微服务之间传递并验证

---

### **阶段 3: 微服务扩展与 Spring Cloud 集成**
目标：集成 Spring Cloud 组件，如 Eureka 服务发现、API 网关等，提升系统的扩展性、服务发现和负载均衡能力。

- [ ] **里程碑 3.1: 集成 Spring Cloud Eureka（服务注册与发现）**
  - 引入 Eureka Server 和 Eureka Client
  - 启用服务注册与发现功能

- [ ] **里程碑 3.2: 集成 Spring Cloud Gateway（API 网关）**
  - 引入 Spring Cloud Gateway 作为 API 网关
  - 配置请求限流、负载均衡和安全认证（如 JWT 验证）

- [ ] **里程碑 3.3: 集成 Spring Cloud Config（配置中心）**
  - 引入 Spring Cloud Config 实现配置的集中化管理
  - 搭建 Config Server 并托管配置文件

---

### **阶段 4: Kubernetes 部署与扩展**
目标：将微服务迁移到 Kubernetes 环境中，实现自动扩展、负载均衡、服务恢复和滚动更新。

- [ ] **里程碑 4.1: 将微服务部署到 Kubernetes 中**
  - 将 Docker 化的微服务部署到 Kubernetes 集群

- [ ] **里程碑 4.2: 实现自动扩展与负载均衡**
  - 配置 Kubernetes 的 Horizontal Pod Autoscaler (HPA)
  - 实现服务实例的自动扩展和负载均衡

- [ ] **里程碑 4.3: 监控与日志管理**
  - 引入 Prometheus 和 Grafana 监控集群
  - 集成 ELK（Elasticsearch + Logstash + Kibana）进行日志收集和分析

---

### **里程碑总结**
1. **阶段 1**：项目初始化，完成基本的用户管理功能和角色权限控制，并在本地进行测试。
2. **阶段 2**：将系统拆分为微服务，并将其容器化，准备进入分布式部署。
3. **阶段 3**：引入 Spring Cloud 组件，提升系统的扩展性、可管理性和容错能力。
4. **阶段 4**：将微服务部署到 Kubernetes 集群，实现分布式架构下的自动扩展、服务发现和监控管理。
