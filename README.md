# Kubernetes Manifests for Jenkins Deployment

Refer https://devopscube.com/setup-jenkins-on-kubernetes-cluster/ for step by step process to use these manifests. &nbsp
Steps: &nbsp
 1. Create namespace devops-tool &nbsp
 2. Create ClusterRole &nbsp
 3. Create ServiceAccount &nbsp
 4. Bind ServiceAccount with the ClusterRole in ClusterRoleBinding &nbsp
 2-4 in ServiceAccount.yaml &nbsp
 5. Create PV and PVC in local storage using volumes.yaml
 6. Create deployment which is the main yaml file for application (here Jenkins) &nbsp
 7. Expose application to outside world using service.yaml we are using the type as NodePort 32000 which will expose Jenkins on all kubernetes node IPs on port 32000. &nbsp 
 8. http://<node-ip>:32000 to see application. nodeip can be got by kubectl get nodes -o wide .. internal ip &nbsp
 9. kubectl logs <podname> -n devops-tools    get hash key from here and paste in jenkins page &nbsp
 10. install plugins &nbsp
  TADA-----------------JENKINS----------------WORKING
