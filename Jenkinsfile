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
       stage('post-deployment'){
          steps{
            
    String HTTP_URL= "https://shashank-kumar-portfolio.netlify.app/"
    description = "<a href='${HTTP_URL}'</a>" + "google"
    manager.addShortText(description, "black", "white", "1.5px", "white");

          }
       }
        
    }
}
