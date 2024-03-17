pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS250-1'
                sh 'g++ new.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
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
            error 'Pipeline Failed'
        }
    }
}