pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git branch:'main', url: 'https://github.com/maimoona-stack/Calculators.git’
      }
    }
    stage('compile') {
      steps {
        sh 'javac Calculators.java'
      }
    }
    stage('build') {
      steps {
        sh 'java Calculators 25 5'
      }
    }
    stage('test') {
      steps {
        sh 'java Calculators 30 -5'
      }
    }
    stage('deploy'){
      steps{
        echo 'Deployment completed'
      }
    }
  }
}

 
