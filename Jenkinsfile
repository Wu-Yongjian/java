pipeline {
    agent any 
 
    stages {
        stage('Test') {
            agent { docker { image 'golang:1.20-alpine' } }
            steps {
                sh '''
                    export http_proxy=1.1.1.1
                    env
                '''
            }
        }
        stage('Build') {
            agent { docker { image 'golang:1.20-alpine' } }
            steps{
                sh '''
                    http_proxy=2.2.2.2
                    env
                '''
            }
        }
}
}
