pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                bat 'gradlew clean build -x test'
            }
        }
        stage('test') {
            steps {
                bat "gradlew test"
            }
        }
        stage('coverage') {
            steps {
                bat 'gradlew jacocoTestReport'
            }
        }
        stage('Analisis de SonarQube') {
            steps {
                withSonarQubeEnv(installationName: 'SonarCloud') {
                    script {
                        bat "gradlew sonarqube -Dsonar.branch.name=main"
                    }
                }
            }
        }
        stage('Sonar') {
            steps {
                bat "gradlew sonarqube"
            {
        }
    }
}