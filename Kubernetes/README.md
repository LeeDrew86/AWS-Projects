# Kubernetes "Hello World" Deployment

## Overview

I explored the fundamentals of containerisation and orchestration by deploying a simple "Hello World" application on Kubernetes.

I developed my ability to:
* Craft Dockerfiles
* Configure Kubernetes manifests
* Use kubectl commands
* Troubleshoot network connectivity

## Steps

1. **Building the Docker Image:**
    * Create a Dockerfile defining the application's environment.
    * Build the image using `docker build`.

2. **Creating Kubernetes Manifests:**
    * Define a deployment manifest outlining pod configuration.
    * Create a service manifest to expose the application.

3. **Deploying to Kubernetes:**
    * Apply the manifests using `kubectl apply`.
    * Monitor deployment status with `kubectl get pods`.

4. **Accessing the Application:**
    * Use `kubectl get service` to find the service's exposed port.
    * Visit the application in a web browser.

## Future Exploration

* Scale the application using `kubectl scale` to observe performance changes.
* Delve into advanced Kubernetes features like volumes and secrets.
* Deploy real-world applications on Kubernetes, leveraging gained knowledge.

