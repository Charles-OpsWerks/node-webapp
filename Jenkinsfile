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
                customImage.inside {
                    sh 'npm start'
                }
            }
        }
    }
}
