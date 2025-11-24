pipeline {
    agent any

    stages {
        stage('Run Tests') {
            steps {
                sh 'pytest --maxfail=1 --disable-warnings'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t calculator-app:latest .'
            }
        }

        stage('Run Calculator Script') {
            steps {
                sh 'python3 calculator.py'
            }
        }
    }
}