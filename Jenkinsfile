pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '/usr/bin/python3 -m venv venv'  // Укажите полный путь к исполняемому файлу Python
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
