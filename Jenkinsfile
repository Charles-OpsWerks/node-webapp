pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t node-app .'
            }
        }
        stage('Run') {
            steps {
                sh 'docker run -d -p 3000:3000 node-app'
            }
        }
        stage('Verify') {
            steps {
                sh 'sleep 10'
                sh 'curl http://localhost:3000'
            }
        }
    }
}
