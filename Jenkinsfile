pipeline{
    agent any
    stages{
        stage ("Deploy to cluster dev-kt-k8s") {
            steps {
                withKubeConfig(credentialsId: 'kubeconfig-dev-kt-k8s') {
                    sh "kubectl apply -f deployment.yaml "
                    sh "kubectl apply -f service.yaml"
                    sh "kubectl apply -f ingress.yaml"
                }
            }
        }
    }
}