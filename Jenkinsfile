pipeline {
    agent any
    stages {
//        stage('Clone repository') {
//            steps {
//                checkout([$class: 'GitSCM',
//                    branches: [[name: '*/main']],
//                    userRemoteConfigs: [[url: 'https://github.com/GLeelakrishna95/PES1UG21CS209_jenkins.git']]])
//            }
//        }
        stage('Build') {
            steps {
                build 'PES1UG21CS209-1'
                sh 'g++ main.cpp -o output'
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

    post{
       failure{
           error 'Pipeline failed'
       } 
    } 
}
