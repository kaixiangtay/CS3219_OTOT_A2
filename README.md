# CS3219_OTOT_TaskA2

**Pre-requisites: Docker and Kubernetes software installed on computer**

Step 1: Clone the project repository onto your local computer.
Step 2: Open up the Terminal and inside the project folder directory, execute the following command to create the application image deployment:
```
kubectl apply -f hello-world.yaml
```
Step 3: Next, execute the following command to create a service object that exposes the deployment:
```
kubectl expose deployment hello-world --type=LoadBalancer --name hello-world-service
```
Step 4: Execute the following command to retrieve the External-Ip and Port:
```
kubectl get services hello-world-service
```
Step 5: Execute the following command using External-Ip and port information from the previous step to access the application:
```
curl http://<external ip>:<port>
```
