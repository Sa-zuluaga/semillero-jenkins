pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                git 'https://github.com/Sa-zuluaga/semillero-jenkins.git'
                echo 'Building..'
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