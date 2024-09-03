pipeline {
    agent any

    stages {
        stage('Build and Run') {
            steps {
                sh 'docker build -t my-node-app .'
                sh 'docker run -p 8080:8080 my-node-app'
            }
        }
    }
}
