pipeline {
    agent any

    tools {
        jdk 'jdk17'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Anand9381/calculator.git'
            }
        }

        stage('Compile') {
            steps {
                sh 'javac Calculator.java Main.java'
            }
        }

        stage('Run') {
            steps {
                sh 'java Main'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
