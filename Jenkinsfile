pipeline {
  agent any
  stages{
    stage('Clone repository'){
      steps{
        checkout([$class: 'GitSCM',
                 branches: [[name: '*/main']],
                 userRemoteConfigs: [[url: 'https://github.com/Tae-Bear/PES2UG21CS227.git']]])
      }
    }
  stage('Build'){
    steps{
    build 'PES2UG21CS227-1'
    sh 'g++ main.cpp -o output'
    }
  }
  stage('Test'){
    error it issss
    steps{
    sh './output'
  }
  }
  stage('Deploy'){
    steps{
      echo 'deploy'
    }
  }
}
post{
  failure{
    error 'Pipeline failed'
    }
  }
}
    
