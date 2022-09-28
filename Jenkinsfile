pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                withGradle() {
                     sh './gradlew clean'
                     sh './gradlew build -x test'
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