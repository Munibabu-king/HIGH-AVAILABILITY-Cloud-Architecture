# HIGH-AVAILABILITY-Cloud-Architecture with Load balancing and RabbitMq Integration

# Project Overview :
    This project presents a cloud-native e-commerce platform built on AWS with load balancing and integrating Redis caching, RabbitMQ messaging, and MySQL for reliability and scalability.By leveraging Kubernetes pods, JWT authentication, and containerized deployments, the system ensures secure, high-availability shopping workflows from login to order delivery.
The solution demonstrates a cost-effective alternative to traditional monolithic platforms, providing fault tolerance, performance optimization, and seamless user experience.
   E-commerce platforms face challenges in handling fluctuating traffic, leading to performance issues during peak times and resource wastage during low traffic. This project builds a scalable, high-availability e-commerce system using AWS EKS, Node.js, and React to ensure seamless performance. The system dynamically scales resources, optimizes costs, and enhances responsiveness with caching (Redis), message queuing (RabbitMQ), and database replication. By leveraging cloud computing and automation, the platform maintains high performance, reliability, and cost efficiency without relying on expensive managed services.

# OBJECTIVE:
Develop a Cost-Effective Cloud Alternative – Build a highly available and scalable web application using most of free, open-source tools instead of using expensive cloud service tools.
 **Implement Intelligent Load Balancing – Use to efficiently distribute incoming traffic across multiple servers, ensuring optimal performance and resource utilization.
 **Enable Automatic Failover Management – Utilize Redis and kubernets & Docker to detect server failures and automatically redirect traffic to healthy servers without manual intervention.
 **Ensure High Availability & Scalability – Design a distributed architecture that supports N-number of servers, dynamically scaling based on real-time traffic demand using Docker and Kubernetes.
 **Optimize Performance & Resource Utilization – Implement efficient caching (Redis), message queuing (RabbitMQ), and database replication to enhance system responsiveness, reduce latency, and ensure smooth handling of high traffic loads.
 
# System Architecture
<img width="1839" height="953" alt="image" src="https://github.com/user-attachments/assets/453f8e36-4020-427a-967f-c806d29c76c0" />







Client -> AWS EKS Cluster (EC2 nodes + Pods) -> Microservices -> 1.user service 2.Catalogue Service 3.Cart Service 4.Payment Service 5.Shipping Service 



Infrastructure:

Redis (Cache)
MySQL (Relational DB)
MongoDB (Product DB)
RabbitMQ (Message Broker)
Kubernetes Services & Deployments

Security

JWT Authentication → secures Cart, Payment, and Shipping APIs.
AWS Security Groups → control inbound/outbound access.

Tech Stack

Frontend: HTML+JS
Backend: Node.js(microservices) 
Databases: MySQL, MongoDB
Cache: Redis
Message Queue: RabbitMQ
Containerization: Docker
Orchestration: Kubernetes (EKS)
Infrastructure: AWS EC2 + EKS
Authentication: JWT 

 # HOW TO RUN
1.	Launch the Home Page
Our website is developed using microservices architecture, with a load balancer integrated in the backend. Users can directly access the homepage of the e-commerce platform, where all available categories and products are displayed in a user-friendly interface.
2.	User Registration
New users click on the Register button, enter their name, email, and contact number. The User Service (secured by JWT) stores user details securely in the database (MongoDB/MySQL).
3.	User Login
Registered users log in using their email/user ID and password. The system authenticates credentials securely, and a token (JWT) is issued for session management, allowing access to the main shopping platform.
4.	Product Browsing and Cart Management
Users browse categories displayed dynamically (AngularJS frontend consuming APIs).
When a user selects an item, it is added to the Cart Service, where cart data is cached using Redis for fast retrieval and smooth user experience.
5.	Order Placement and Payment Processing
Users proceed to the Cart page, adjust item quantities, and confirm the shipping address.
On checkout, the Payment Service handles secure transactions, updates order status, and RabbitMQ queues update notifications between services.
6.	Order Confirmation and Completion
After successful payment, users receive an "Order Successful" confirmation message.
The Shipping Service tracks and updates delivery status dynamically. Ratings and feedback options become available after order fulfillment.


# Results


Achieved Web Application withhigh availability via Kubernetes LoadBalancer service.

Improved performance using Redis caching.

Ensured reliability with RabbitMQ queues.

Secured user authentication with JWT.

Delivered a complete shopping workflow: browse → cart → checkout → shipping.

