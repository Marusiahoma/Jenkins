pipeline {
    agent {
        docker { 
            image 'python:latest' 
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'python -m venv venv'
                sh 'source venv/bin/activate && pip install -r requirements.txt'
            }
        }
    }
    post {
        success {
            archiveArtifacts artifacts: ['main.py', 'requirements.txt'], fingerprint: true
        }
    }
}

