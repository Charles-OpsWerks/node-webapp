pipeline {
    agent any

    stages {
        stage('Build and Run') {
            steps {
                checkout scm

                docker.build("my-app:${env.BUILD_ID}").run()
            }
        }
    }
}
