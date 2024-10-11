pipeline {
    agent any

    environment {
        KUBECONFIG = "${env.HOME}/.kube/config" // Path to your kubeconfig file
    }

   stage {
      stage ('Deploying in k8s') {
         steps {
            sh 'sudo kubectl create -f hello-world.yaml'
            sh 'sudo kubectl apply -f hello-world-ingress.yaml'
         }
      }
  }
}
