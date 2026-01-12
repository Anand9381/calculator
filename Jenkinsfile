pipeline {
    agent any

    tools {
        jdk 'jdk11'
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
                bat 'javac Calculator.java Main.java'
            }
        }

        stage('Run') {
            steps {
                bat 'java Main'
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
