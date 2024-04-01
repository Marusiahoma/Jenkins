pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '/var/lib/jenkins/workspace/Project1/.git -m venv venv'  // Укажите полный путь к исполняемому файлу Python
                sh 'source venv/bin/activate && pip install -r requirements.txt'
            }
        }
    }
    post {
        success {
            archiveArtifacts artifacts: ['test_main_page.py', 'requirements.txt'], fingerprint: true
        }
    }
}
