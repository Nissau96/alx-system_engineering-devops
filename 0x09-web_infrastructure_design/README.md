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