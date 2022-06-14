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
              sh 'cd git-cicd'
            }
        }
        stage ('Install'){
             steps {
  
        sh 'cd git-cicd'
   //sh 'cd git-cicd'
      sh 'ls'

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
