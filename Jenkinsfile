pipeline {
    agent any

    stages {
        stage('Run Tests') {
            steps {
                sh 'pytest'
            }
        }

        stage('Run Calculator Script') {
            steps {
                sh 'python3 calculator.py'
            }
        }
    }
}