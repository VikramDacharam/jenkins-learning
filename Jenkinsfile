/* pipeline {
    agent {
      node {
        label 'ansible'
    }
  }

  options {
    disableConcurrentBuilds()
    ansiColor('xterm')
  }
  // triggers { cron('*//*  *//* 5 * * * *') }
     triggers { pollSCM('*//*  *//* 1 * * * *') }

  parameters {
    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
    booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
    choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
    password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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
         sh 'echo -e "\\e[31mHello"'
         echo PERSON
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
} */
// node{
//  stage('Test') {
//   echo "Test completed"
//  }
//
//  stage('Test1') {
//    echo "Test1 completed"
//  }
//  }


pipeline {
  agent {
        node {
          label 'ansible'
      }
    }
  tools {
    maven 'maven'
  }

  stages{
    stage('One') {
      input {
        message "will you approve?"
        ok "Yes"
        submitter "admin"
        parameters {
          string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                      }
      }
      steps{
       // sh 'mvn --version'
       sh 'echo PERSON=${PERSON}'
      }
    }
  }
}


