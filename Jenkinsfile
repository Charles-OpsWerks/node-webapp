pipeline {
    agent any

    stages {
        stage('Build and Run') {
            steps {
                sh '/usr/bin/docker build -t my-node-app .'
                sh '/usr/bin/docker run -p 3000:3000 my-node-app'
            }
        }
    }
}
