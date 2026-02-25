pipeline {
agent any
stages {
stage('clone') {
steps {
git branch:'main', url: 'https://github.com/sowjanya-it/Jenkinsjavaparam.git’;
}
}
stage('compile') {
steps {
sh 'javac Calculator.java'
}
}
stage('build') {
steps {
sh 'java Calculator 25 5'
}
}
  stage('Deploy'){
    step{
      echo "deployment completed'
    }
  }
}
}
