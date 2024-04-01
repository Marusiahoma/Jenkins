pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '/usr/bin/python3 -m venv venv'
                sh '. venv/bin/activate'
                sh 'pip install -r requriment.txt'
            }
        }
    }
   post {
    success {
        archiveArtifacts artifacts: 'TheResult.exe', fingerprint: true
    }
}
}

