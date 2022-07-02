pipeline {
  agent {
    node {
      label 'ansible'
    }
  }

  environment {
    DEMO_URL = "google.com"
    SSH = credentials("SSH")

  }

  stages {

     stage('Test') {
       environment {
         DEMO_URL = "yahoo.com"
       }
       steps{
         echo 'Hello world'
         echo DEMO_URL
         echo SSH
       }
     }
      stage('Test1') {
        steps{
          echo 'Hello world'

        }
      }
   }

   post {
     always {
       echo 'OK'
     }
   }
}
//node{
//  stage('Test') {
//   echo "Test completed"
//  }
//
//  stage('Test1') {
//    echo "Test1 completed"
//  }
//  }