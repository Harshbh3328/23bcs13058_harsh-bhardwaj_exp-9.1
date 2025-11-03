# Dockerize React App (Multi-Stage Build)

This project demonstrates a minimal React app packaged using a multi-stage Docker build for production.

## Steps

1. **Build Docker image**
   ```bash
   docker build -f docker/Dockerfile -t react-multistage .

2. Run container

docker run -p 80:80 react-multistage

3. Open http://localhost
 to view the app.

Why Multi-Stage?

First stage: uses Node to build the React app.

Second stage: copies only production build into Nginx → smaller image.
