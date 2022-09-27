pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh "gradlew clean"
                sh "gradlew build -x test"

            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh "gradlew test"
                sh "gradlew jacocoTestReport"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}