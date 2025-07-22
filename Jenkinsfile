pipeline {
    agent any

    environment {
        VENV = "venv"
    }

    stages {
        stage('Checkout') {
            steps {
                git credentialsId: 'github-creds', url: 'https://github.com/mohdsalim1316/Ping-Pong.git/'
            }
        }

        stage('Build') {
            steps {
                sh '''
                    python3 -m venv $VENV
                    source $VENV/bin/activate
                    pip install -r requirements.txt
                '''
            }
        }
    }
}
