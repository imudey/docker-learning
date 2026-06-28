🐳 CoderCo Containers Challenge
📌 Overview

This project is part of the CoderCo Containers Challenge, where I built and deployed a multi-service containerized application using Docker Compose.

The system consists of:

A Flask web application
A Redis database for tracking visits
An Nginx reverse proxy
A Docker Compose setup with scaling enabled

The goal was to learn how multiple services communicate inside a containerized environment and how to debug real-world Docker issues.

🏗️ Architecture
Browser
   ↓
Nginx (reverse proxy)
   ↓
Flask Web App (scaled to 3 replicas)
   ↓
Redis (visit counter storage)
🚀 How to Run the Project
git clone <your-repo-url>
cd coderco-challenge
docker compose up --build --scale web=3

Then open:

http://127.0.0.1:5002

Test visit counter:

http://127.0.0.1:5002/count
🧠 What I Learned
🐳 Docker & Docker Compose
How to define and manage multi-container applications
How services communicate using Docker networking

How to scale services using:

--scale web=3
How container port mapping works (HOST:CONTAINER)
🌐 Nginx Reverse Proxy
How Nginx forwards requests to backend services
How upstream load balancing works with multiple replicas
Importance of correct nginx.conf structure
🐍 Flask in Containers
Running Flask apps inside Docker containers
Binding Flask to 0.0.0.0 for external access
Creating REST endpoints (/ and /count)
🔴 Redis Integration
Using Redis as a lightweight in-memory database
Incrementing values across requests (INCR)
Connecting services using Docker service names (redis)
🧩 Debugging Skills Gained
Fixing YAML indentation and structure issues
Debugging container startup failures (Created, Exited)

Understanding logs using:

docker compose logs
Diagnosing network and port exposure problems
⚠️ Key Challenges Faced
Incorrect Docker Compose indentation
Nginx container failing due to invalid configuration
Redis connection issues caused by environment variable mistakes
Misunderstanding of Docker port mapping
Debugging multi-service communication issues
📈 Outcome

Successfully built and deployed a working containerized system with:

Load-balanced Flask services
Persistent Redis state tracking
Reverse proxy routing via Nginx
Scalable architecture using Docker Compose
🏁 Conclusion

This project significantly improved my understanding of containerized systems and real-world debugging workflows. I now have a much clearer grasp of how microservices communicate, how Docker networking works, and how to troubleshoot multi-container applications effectively.
