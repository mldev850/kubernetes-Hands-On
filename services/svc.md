### Services
- Abstract Pod details to facilitate connectivity

### Project
 - docker pull lmacademy/colorapi:1.0.0
 - docker pull lmacademy/trafficgenrator:1.0.0
 - color-api.yaml


 ### Working with ClusterIP services
 


### NodePort Services
 - kubectl get node -o wide ( Internal ip is not related to k8's cluster it is a seperate kind of VM )
 - kubectl get pod -o wide ( To check pod runs on which node )
 - To access use <NODE_IP>:30007
 - u can curl <POD_IP>
 - Nodeport service using this particular service we can able to access the application with the help of nodeip and nodeport

### External Name Service
 - In yaml externalName must be dns like google.com. Not http://google.com
 - kubectl exec -it traffic-generator -- sh
 - curl <external_service_name>
