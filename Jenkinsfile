pipeline {
    agent any
    stages {
        stage('build-and-push-docker-image') {
            steps {
                build_and_push_docker_image()
            }
        }
    }
}

def build_and_push_docker_image(){
    echo "Building docker image.."
    sh "docker build --no-cache -t romansasacovs/api-tests:latest ."

    echo "Pushing docker image"
    sh "docker push romansasacovs/api-tests:latest"
}