pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000 -p 5000:5000' 
        }
    }
    stages {
        environment {
            CI = 'true'
        }
        stage('Build') {
            steps {
                sh 'echo "Hello world!"'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}
