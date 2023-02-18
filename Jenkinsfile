pipeline {
    agent any

stages{
  stage('Build') {
     steps{
        sh 'g++ -o PES2UG20CS063 PES2UG20CS063.cpp'
    }
  }

  stage('Test') {
    steps{
       sh './PES2UG20CS063';
    }
  }

  stage('Deploy') {
    steps{
      echo 'DEPLOYMENT SUCCESSFUL FROM GITHUB REPO - PES2UG20CS063_Jenkins'
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
