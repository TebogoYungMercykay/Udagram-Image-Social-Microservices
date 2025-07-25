# Deployment Documentation

![Image](./images/screenshots/image-16.png)

> This project uses CircleCI for Continuous Integration and Deployment. Below are the screenshots demonstrating the infrastructure setup and deployment pipeline.

## Kubernetes Deployment

#### Application Running

Screenshot showing the application running successfully in the browser:

![Image](./images/screenshots/image-20.png)

![Image](./images/screenshots/image-12.png)

#### Pods Verification

To verify Kubernetes pods are deployed properly:

```bash
kubectl get pods
```

![Image](./images/screenshots/image-16.png)

![Image](./images/screenshots/image-10.png)

![Image](./images/screenshots/image-09.png)

#### Horizontal Pod Autoscaler (HPA)

To verify horizontal scaling is configured against CPU usage:

```bash
kubectl get hpa
```

![Image](./images/screenshots/image-17.png)

#### Services Configuration

To verify Kubernetes services are properly configured:

```bash
kubectl describe services
```

![Image](./images/screenshots/image-18.png)

![Image](./images/screenshots/image-19.png)

#### Application Logging

To verify logging is set up with backend applications:

```bash
kubectl logs {pod_name}
```

![Image](./images/screenshots/image-21.png)

![Image](./images/screenshots/image-22.png)

## Continuous Integration & Deployment Pipeline

#### Docker Locally

Verifying that Docker images running containers on the local machine before pushing them to DockerHub.

```bash
docker images
docker ps
```

![Image](./images/screenshots/image-04.png)

![Image](./images/screenshots/image-03.png)

#### DockerHub Container Registry

DockerHub repository showing the containers that have been pushed:

![Image](./images/screenshots/image-13.png)

![Image](./images/screenshots/image-07.png)

![Image](./images/screenshots/image-15.png)

![Image](./images/screenshots/image-14.png)

#### CircleCI Webhook Integration

GitHub repository settings showing the CircleCI webhook configuration (Settings → Webhooks):

![Image](./images/screenshots/image-23.png)

#### CircleCI Build Success

CircleCI dashboard showing successful build and deployment jobs:

![Image](./images/screenshots/image-06.png)

---

## Infrastructure Review

To help review the infrastructure setup, the above screenshots demonstrate:

1. **Kubernetes Cluster Health**: All pods are running successfully
2. **Service Discovery**: Kubernetes services are properly configured
3. **Auto-scaling**: HPA is configured for CPU-based scaling
4. **Monitoring & Logging**: Application logs are accessible via kubectl
5. **Container Registry**: Docker images are successfully pushed to DockerHub
6. **CI/CD Pipeline**: CircleCI is integrated with GitHub and executing successful deployments

This confirms that the microservices architecture is properly deployed and the continuous integration pipeline is functioning as expected.

---
