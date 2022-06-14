pipeline {
   agent any
     tools {nodejs "nodejs"}
    environment {
        CI = 'true'
    }
    stages {      
        stage('Build') {
            steps {
           // sh  'git clone https://github.com/shashank-kumar-rajput/git-cicd.git'
             // sh 'cd git-cicd'
               echo 'New Build'
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
        }
        stage ('Install'){
             steps {
  
        echo 'New update'

      }
        }
        stage('Test') {
            steps {
                 //sh 'npm test'
                 echo 'New Commit'
            }
        }
       
        
    }
}
