pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                withgradle() {
                    sh "./gradlew -v"
                }

            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}