pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                // Clones the source code from the provided Git repository
                git branch: 'main', url: 'https://github.com/learner2845/raghu.git'
            }
        }
        stage('Build') {
            steps {
                // Builds the Docker image
                sh "docker build -t localhost:5000/python-demo:v1 ."
            }
        }
        stage('Push') {
            steps {
                // Pushes the Docker image to the local Docker registry
                sh "docker push localhost:5000/python-demo:v1"
            }
        }
    }
}
