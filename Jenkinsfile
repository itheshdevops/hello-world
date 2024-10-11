pipeline {
    agent any

    environment {
        KUBECONFIG = "/root/.kube/config" // Path to your kubeconfig file
    }

   stages {
      stage ('Deploying in k8s') {
         steps {
            sh 'sudo /root/bin/kubectl create -f hello-world.yaml'
            sh 'sudo /root/bin/kubectl apply -f hello-world-ingress.yaml'
         }
      }
  }
}
