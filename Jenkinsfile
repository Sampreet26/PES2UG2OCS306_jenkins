pipeline{
  agent any
  stages{
  stage('Build') {
    steps{
      sh 'g++ -o PES2UG20CS306 PES2UG20CS306.cpp'
    }
  }

  stage('Test') {
    steps{
       sh './PES2UG20CS30'
    }
  }

  stage('Deploy') {
    steps{
      echo 'DEPLOYMENT SUCCESSFUL'
    }
  }
  }

  post {
    failure {
        echo 'Pipeline Failed'
    }
  }
}
