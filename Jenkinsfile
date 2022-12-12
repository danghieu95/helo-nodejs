pipeline {
    agent any
    stages {
        stage ('Clone') {
            steps  {
                git 'https://github.com/danghieu95/helo-nodejs.git'
            }
        }
        stage ('Build') {
            steps  {
                withDockerRegistry(credentialsId: 'docker-hub', url: 'https://index.docker.io/v1/') {
                    sh 'docker build -t xindunglangim/hello-nodejs:v10 .'
                    sh 'docker push xindunglangim/hello-nodejs:v10 '
                }
            }
        }
    }
}
