pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build app'
            }
        }
        stage('Test') {
            steps {
                echo 'Test app'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy app'
            }
        }
    }
    post{
        always{
            emailext body: '', subject: 'Demo Pipeline', to: 'shetesrushti11@gmail.com'
        }
    }
}
