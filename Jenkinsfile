pipeline {
    agent any

    stages {
        stage('Check Out') {
            steps {
                echo 'Checking out... GIT_COMMIT:'
                echo "${env.GIT_COMMIT}"
                echo "Files updated!!!"
                bat "git show --pretty='' --name-only -r ${env.GIT_COMMIT}"
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
