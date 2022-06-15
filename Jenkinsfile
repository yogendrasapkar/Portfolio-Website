pipeline {
   agent any
     tools {nodejs "nodejs"}
    environment {
        CI = 'true'
    }
    stages {      
        stage('Build') {
            steps {
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
                env.NODE_ENV = "test"

            print "Environment will be : ${env.NODE_ENV}"

         sh 'node -v'
         sh 'npm prune'
         sh 'npm install'
         sh 'npm test'
            }
        }
    }
       post {
            success {
                echo "Test run completed succesfully."
               echo "Sending Email to : kumar.shashank@kiet.edu"
                mail(from: "shashank.1721ec1128@kiet.edu",
                to: "kumar.shashank@innovaccer.com",
                subject: "Job build ${env.BUILD_ID} passed  ",
                body: "Build : ${env.BUILD_ID} on ${env.JENKINS_URL} Job: ${env.BUILD_URL}")
            }
            failure {
                echo "Test run failed."
               echo "Sending Email to : kumar.shashank@kiet.edu"
                mail(from: "shashank.1721ec1128@kiet.edu",
                to: "kumar.shashank@innovaccer.com",
                subject: "Job build ${env.BUILD_ID} failed ",
                body: "Hi, Kindly check the error for the following details : Build : ${env.BUILD_ID} on ${env.JENKINS_URL} Job: ${env.BUILD_URL}")
            }
            always {
                deleteDir()
                echo "Workspace cleaned"
            }
    } 
}
