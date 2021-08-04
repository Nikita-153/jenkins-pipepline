pipeline {
    agent any
    
    stages {
        stage('Check Out') {
            steps {
                
                echo 'Checking out... GIT_COMMIT:'
                echo "${env.GIT_COMMIT}"
                echo "Files updated!!!"
//                  bat "git show --name-only --pretty=format:"
              script {
//                 def script = '''set status=FALSE 
//                                 echo %status%''' 
//                 def status = bat(script: script, returnStdout: true)
//                 echo "$status" 
                  
                def stdout = bat(returnStdout: true, script: 'git show --name-only --pretty=format:').split("\n")
                println("stdout value is:\n" + stdout)  
                  for(int i = 0; i<stdout.length; i++ ){
                        println(stdout[i])
                  }
                } // End of script
                
            } // End of step
        } // End of stage
        
        
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
