pipeline {
    
    agent any

    stages {

        stage ('Build Docker Image') {
            steps {
                script {
                    dockerapp = docker.build("cabicho/iniciativa_dev_ops_kube_news:${env.BUILD_ID}",'-f ./src/Dockerfile ./src')
                }
            }
        }
    }
}