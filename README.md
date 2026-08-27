# ShiftSync — API Gateway

**Student Name:** Chamith Bhanuka Widanapathirana  
**Student ID / Number:** 241711051  
**Slack Handle:** Chamith Bhanuka  
**GCP Project ID:** project-a58ee7a4-4913-4af2-a6d  
**Course:** ITS 2130 — Enterprise Cloud Architecture  

---

## Description

Central API Gateway for the ShiftSync enterprise platform built with Spring Boot and Spring Cloud Gateway MVC. Serves as the single ingress routing point for client applications to access backend domain microservices discovered dynamically via Netflix Eureka.

---

## Key Responsibilities

- **Dynamic Routing**: Dispatches `/api/scheduling/**`, `/api/notifications/**`, and `/api/credentials/**` to corresponding microservices via Eureka service discovery (`lb://SCHEDULING-SERVICE`, `lb://NOTIFICATION-SERVICE`, `lb://CREDENTIAL-SERVICE`).
- **Load Balancer Health Check**: Provides dedicated health endpoints (`/health`, `/actuator/health`, `/`) for Google Cloud Load Balancer health probes (`hc-api-gateway`).
- **Cross-Origin Resource Sharing (CORS)**: Configured to support web applications and Cloud Run frontends.

---

## Technology Stack

- Java 25
- Spring Boot 3.x
- Spring Cloud Gateway MVC
- Spring Cloud Netflix Eureka Client
- Spring Cloud Config Client
