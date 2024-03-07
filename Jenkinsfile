pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM',
                          branches: [[name: '*/main']],
                          userRemoteConfigs: [[url: 'https://github.com/Sumedh220122/PES1UG21CS465_Jenkins.git']]])
            }
        }

        stage('Build') {
            steps {
                sh 'g++ main.cpp -o output'
            }
        }

        stage('Test') {
            steps {
                sh './outpu'
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
