pipeline {
    agent any
    environment {
        DOCKER_EXE = '/usr/bin/docker'
    }
    stages {
        stage('Build') {
            steps {
                checkout scm
                sh '${DOCKER_EXE} build -t node-app:19 .'
            }
        }
        stage('Run') {
            steps {
                sh '${DOCKER_EXE} run -p 3000:3000 node-app:19'
            }
        }
    }
}
