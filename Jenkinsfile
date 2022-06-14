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
               echo "Running Build : ${env.BUILD_ID} on ${env.JENKINS_URL} Job: ${env.BUILD_URL}"
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
       post {
            success {
                echo "Test run completed succesfully."
                mail(from: "shashank.1721ec1128@kiet.edu",
                to: "kumar.shashank@innovaccer.com",
                subject: "Job build passed ",
                body: "Build : ${env.BUILD_ID} on ${env.JENKINS_URL} Job: ${env.BUILD_URL}")
            }
            failure {
                echo "Test run failed."
                mail(from: "shashank.1721ec1128@kiet.edu",
                to: "kumar.shashank@innovaccer.com",
                subject: "Job build failed ",
                body: "Hi, Kindly check the error for the following details : Build : ${env.BUILD_ID} on ${env.JENKINS_URL} Job: ${env.BUILD_URL}")
            }
            always {
        // Let's wipe out the workspace before we finish!
                deleteDir()
                echo "Workspace cleaned"
            }
    }
  

    
   
}
