pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/prakashpanda28901-creator/flask-security-demo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }

        stage('SonarQube Scan') {
            steps {
                withSonarQubeEnv('SonarQube') {

                    bat 'sonar-scanner'
                }
            }
        }
    }
}
