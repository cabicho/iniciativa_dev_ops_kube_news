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

        stage ('Push Docker Image') {
            steps {
                script {
                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') app = docker.build("cabicho/iniciativa_dev_ops_kube_news:${env.BUILD_ID}",'-f ./src/Dockerfile ./src')
                        dockerapp.push('latest')
                        dockerapp.push("${env.BUILD_ID}")
                }
            }
        }
    }
}