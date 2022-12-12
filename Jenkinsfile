pipeline {
    agent any
    stages {
        stage ('Clone stage') {
            steps  {
                git credentialsId: 'hello', url: 'https://github.com/danghieu95/helo-nodejs.git'
            }
        }
    }
}
