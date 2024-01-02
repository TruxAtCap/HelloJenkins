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
        stage('podman Build') {
            steps {
               sh 'podman images -a'
               sh """
               podman container list -a
               podman pull alpine
               podman run --rm alpine cat /etc/hostname
               podman container list -a
               """
            }
        }
    }
}
