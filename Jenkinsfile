pipeline {
    agent {
        docker {
            image 'node:latest'
            args '-p 3000:3000'
        }
    }

    stages {
        stage('Build') {
            steps {
                checkout scm
                sh 'docker build -t node-app:19 .'
            }
        }
        stage('Run') {
            steps {
                sh 'docker run -p 3000:3000 node-app:19'
            }
        }
    }
}
