pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'g++ working.cpp -o working'
      }
    }
   
    stage('Test') {
      steps {
        sh './working'
      }
    }
   
    stage('Deploy') {
      steps {
        sh '/departent/services'
      }
    }
  }
 
  post {
    failure {
       
          echo 'Pipeline failed'
        }
    }
   
  }
