pipeline {

    agent {
        label 'thinkpad'
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Downloading code from GitHub...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'No build required'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                mkdir -p /home/pranjal/deployments/demo-app
                cp -r * /home/pranjal/deployments/demo-app/
                '''
            }
        }
    }

    post {
        success {
            echo 'Deployment Successful'
        }

        failure {
            echo 'Deployment Failed'
        }
    }
}
