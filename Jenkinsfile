pipeline {
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'g++ main/hello.cpp'
        build 'PES2UG20CS206-1'
        echo 'Build Successful'
      }
    }
    stage('Test'){
      steps{
        sh './a.out'
      }
    }
    stage('Deploy') {
      when {
        expression {
          currentBuild.result == null || currentBuild.result == 'SUCCESS' 
        }
      }
      steps {
        echo 'Deployment Successful'
      }
    }
  }
}
