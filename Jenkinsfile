pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh './gradlew assemble'
            }
        }
        stage('Test') {
            steps {
                sh './gradlew test'
            }
        }
    }

    post {
        success {
            echo 'Build and Test succeeded!'
        }
        failure {
            echo 'Build or Test failed!'
        }
    }
}
