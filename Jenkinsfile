pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                withGradle() {
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