pipeline {
    agent any

    stages {
        stage('Preparation') {
            steps {
                cleanWs()
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'bash ./sample-app.sh'
            }
        }

    }

    post {
        always {
            cleanWs()
        }
    }
}
