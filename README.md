# kubernetes-deployments
This will have all the code with kubernetes from basics to advanced , we will be integrating lot of services with kubernetes to make our life easier.

You can do a basic deployment of a tomcat application from the Tomcat-Deployment
To start of with the deployment you should be having a cluster running , you can setup minikube for the same
Deploy the namespace.yaml file for creating the namespace dev
Deploy the deployment.yaml with the command "kubectl apply -f deployment.yaml"
Deploy the service file with the command "kubectl apply -f service.yaml"

Check for the status of deployments with th command kubectl get all -n dev , output will show you the atatus of everything deployed in the "dev" namespace.

now in order to check your application , you can do a portforwarding to your localhost port with the command
kubectl port-forward service/service_name 8080(localhost_port):8080(remote_port) -n dev (porting localhost port with the pod/container port)
you can run the application in your browser by typing out this localhost:8080.

