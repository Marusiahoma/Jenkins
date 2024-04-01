pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'python -m venv venv'
                sh '. /var/lib/jenkins/workspace/Project1 && pip install -r requirements.txt'
            }
        }
    }
    post {
        success {
            archiveArtifacts artifacts: ['test_main_page.py', 'requirements.txt'], fingerprint: true
        }
    }
}
