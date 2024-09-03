pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                checkout scm
                def customImage = docker.build("node-app:${env.BUILD_ID}")
            }
        }
        stage('Run') {
            steps {
                sh "docker run -p 3000:3000 node-app:${env.BUILD_ID}"
            }
        }
    }
}
