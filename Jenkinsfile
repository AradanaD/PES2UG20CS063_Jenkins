pipeline {
    agent any

stages{
  stage('Build') {
    steps{
        sh 'g++ -o PES2UG20CS367 PES2UG20CS367.cpp'
    }
  }

  stage('Test') {
    steps{
       sh './PES2UG20CS367'
    }
  }

  stage('Deploy') {
    steps{
      echo 'DEPLOYMENT SUCCESSFUL FROM GITHUB REPO - PES2UG20CS367_Jenkins'
    }
  }
}
post {
    always {
      echo 'Pipeline was completed'
    }
    failure {
        echo 'Pipeline has Failed'
    }
  }
}
