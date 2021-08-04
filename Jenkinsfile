pipeline {
    agent any
    
    stages {
        stage('Check Out') {
            steps {
                
                echo 'Checking out... GIT_COMMIT:'
                echo "${env.GIT_COMMIT}"
                echo "Files updated!!!"
                // bat "git show --name-only --pretty=format:"
                
                def stdout = bat(returnStdout: true, script: 'git show --name-only --pretty=format:')
                println("stdout ################ " + stdout + " ####################")
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
