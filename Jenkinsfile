node {
    checkout scm

    // Run a Docker container with Docker installed
    def dockerImage = docker.build("docker:dind")
    dockerImage.inside {
        // Run the Docker build command inside the container
        sh 'docker build -t node:lts-slim ./'
    }
}
