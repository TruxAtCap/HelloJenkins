pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Verify Branch') {
            steps {
               echo "$GIT_BRANCH"
            }
        }
        stage('Docker Build') {
            steps {
               sh 'podman images -a'
            }
        }
    }
}
