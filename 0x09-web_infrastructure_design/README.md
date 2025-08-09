# 0x09. Web Infrastructure Design

This project covers the fundamentals of web infrastructure design. It starts with a simple, single-server stack and progressively introduces concepts like redundancy, load balancing, and monitoring to build a more robust and scalable system.

## Learning Objectives 🧠

At the end of this project, I will be able to:
* Diagram a web stack from simple to complex architectures.
* Explain the role and interaction of each component (DNS, Load Balancer, Web Server, App Server, Database).
* Explain system redundancy and its importance in eliminating single points of failure (SPOF).
* Define and understand acronyms like LAMP, SPOF, and QPS.

---

## Project Structure

- `0-simple_web_stack`: Diagram and explanation of a basic LAMP stack on a single server


## Task 0: Simple Web Stack

### Overview
A basic web infrastructure with:
- 1 server hosting all components
- Nginx web server
- Application server
- MySQL database
- Domain name (foobar.com) with www record pointing to server IP

### Key Concepts Explained
- **Server**: The physical/virtual machine hosting our services
- **DNS**: Translates human-readable domain names to IP addresses
- **Web Server**: Handles HTTP requests and serves content
- **Application Server**: Executes business logic
- **Database**: Persistent data storage

### Limitations
1. Single Point of Failure (SPOF)
2. Maintenance causes downtime
3. No scalability

### 📄 Task 1: Distributed web infrastructure

A design that introduces a load balancer and distributes web infrastructure components across three servers.

* **File:** `1-distributed_web_infrastructure`
* **Description:** This design separates the web server, application server, and database onto different machines and adds a load balancer (HAProxy) as the entry point. It explains concepts like load-balancing algorithms, Active-Active setups, and Primary-Replica database clusters. It also identifies the remaining SPOFs and security vulnerabilities.

### 📄 Task 2: Secured and monitored web infrastructure

A design that adds security and observability to the distributed infrastructure by implementing firewalls, HTTPS, and monitoring.

* **File:** `2-secured_and_monitored_web_infrastructure`
* **Description:** This architecture secures the 3-server setup with firewalls on each host and encrypts traffic using an SSL certificate on the load balancer. It also adds monitoring clients to each server for data collection. The design highlights key issues like the risk of SSL termination and the SPOF of a single write-database.