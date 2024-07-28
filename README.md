**E-commerce System Backend**

This project is an efficient and scalable E-commerce backend system built using a microservice architecture provided in the resource. The backend consists of three main microservices: User service, Product service, and Cart service. The system is containerized using Docker and managed with Docker Compose. Nginx is used as a reverse proxy to route requests to the appropriate microservice.

**Microservices**

- User Service: Manages user profiles, authentication, and authorization.
- Product Service: Manages the product catalog, including product details and inventory.
- Order service: Handles cart-related operations such as adding items to the cart and checkout.

**Prerequisites**

- Docker: Install Docker.
- Docker Compose: Install Docker Compose.
- Git: Install Git.

**Getting Started**

**Clone the Repository**

git clone https://github.com/yourusername/ecommerce-backend.git
cd ecommerce-backend

**Build and Run the Containers**

Build and start all services using Docker Compose:

docker-compose up --build

This command builds the Docker images for each microservice and starts the containers. Nginx will be running on port 80.

**CI/CD Pipeline**

GitHub Actions

This project uses GitHub Actions for continuous integration and continuous deployment. The workflow file is located in .github/workflows/ci-cd.yml. It triggers on pushes to the main branch and performs the following steps:

1. Checkout the repository.
2. Set up Docker Buildx.
3. Log in to Docker Hub.
4. Build Docker images for each microservice and push them to Docker Hub.

**Deployment Script**

The deployment script (deploy.sh) pulls the latest Docker images from Docker Hub and restarts the microservices using Docker Compose. It logs deployment details and handles errors gracefully.