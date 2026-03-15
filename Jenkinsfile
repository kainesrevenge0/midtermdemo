pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/kainesrevenge0/midtermdemo.git'
            }
        }

        stage('Build') {
            steps {
                sh './mvnw clean package'
            }
        }

        stage('Test') {
            steps {
                sh './mvnw test'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
            }
        }

    }
}
