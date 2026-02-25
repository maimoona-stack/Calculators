pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                // Fixed the curly quote at the end of the URL
                git branch: 'main', url: 'https://github.com/maimoona-stack/Calculators.git'
            }
        }

        stage('Compile') {
            steps {
                sh 'javac Calculators.java'
            }
        }

        stage('Build/Package') {
            steps {
                // Usually, 'build' involves creating a JAR, 
                // but if you are just running it, we'll keep the execution here.
                sh 'java Calculators 25 5'
            }
        }

        stage('Test') {
            steps {
                // Running a second execution to simulate a test case
                sh 'java Calculators 30 -5'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment completed successfully!'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline execution finished.'
        }
        failure {
            echo 'Pipeline failed. Check the console output for errors.'
        }
    }
}
