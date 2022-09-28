pipeline {
    agent any
    tools {
        gradlew
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                withGradle()    {
                     sh './gradlew clean'
                     sh './gradlew build -x test'
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                withGradle{
    {               sh "./gradlew test"
                    sh "./gradlew jacocoTestReport"
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}