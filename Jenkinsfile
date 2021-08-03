pipeline {
    agent any

    stages {
        stage('Check Out') {
            steps {
                echo 'Checking out... ;)'
                echo "${env.GIT_COMMIT}"
            }
        }
         stage('Build') {
            steps {
                echo 'Building...'
            }
        }
         stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
         stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
