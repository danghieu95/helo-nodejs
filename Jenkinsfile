pipeline {
    agent any
    stages {
        stage ('Clone stage') {
            steps  {
                git credentialsId: 'hello', url: 'https://github.com/danghieu95/helo-nodejs.git'
            }
        }
        stage ('Build stage') {
            steps  {
                withDockerRegistry(credentialsId: 'docker-hub', url: 'https://index.docker.io/v1/') {
                    sh label: '', script: 'docker build -t xindunglangim/hello-nodejs:v10 .'
                    sh label: '', script: 'docker push xindunglangim/hello-nodejs:v10 '
                }
            }
        }
    }
}
