pipeline {
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'g++ hello.cpp'
        build 'PES2UG20CS206-1'
        echo 'Build Successful'
      }
    }
    stage('Test'){
      steps{
        sh './a.out'
      }
    }
    stage('Deploy'){
      sh './a.out'
    }
  }
}
