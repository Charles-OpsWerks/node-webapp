pipeline {
    agent any

    stages {
        stage('Build and Run') {
            steps {
                sh 'docker build -t my-node-app .'
                sh 'docker run -p 3000:3000 my-node-app'
            }
        }
    }
}
