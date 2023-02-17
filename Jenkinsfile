pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'g++ working.cpp -o working'
        build job: "PES2UG20CS531", wait: true
      }
    }
   
    stage('Test') {
      steps {
        sh './working'
      }
    }
   
    stage('Deploy') {
      steps {}
    }
  }
 
  post {
    failure {
       
          echo 'Pipeline failed'
        }
    }
   
  }
