pipeline {
    agent any

    stages {
        stage('Build and Run') {
            steps {
                checkout scm

                def customImage = docker.build("my-image:${env.BUILD_ID}", "./")

                customImage.inside {
                    sh 'npm start'
                }
            }
        }
    }
}
