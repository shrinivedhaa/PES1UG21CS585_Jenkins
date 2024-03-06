pipeline {
    agent any 
    stages {
      stage('Build') {
        steps {
          build 'PES1UG21CS585-1'
          sh 'g++ PES1UG21CS585.cpp -o PES1UG21CS585'
        }
      }

      stage('Test') {
        steps {
            sh './PES1UG21CS585hello'
        }
      }

      stage('Deploy') {
        steps {
          echo 'deploy'
        }
      }
    }
    post {
      failure {
        error 'Pipeline failed'
      }
    }
}
