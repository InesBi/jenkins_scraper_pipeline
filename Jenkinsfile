pipeline {
    agent any

    stages {
        stage('Install dependencies') {
            steps {
                sh 'python3 -m venv venv'
                sh '. venv/bin/activate && pip install -r requirements.txt'
            }
        }

        stage('Run scraper') {
            steps {
                sh '. venv/bin/activate && python3 scraper.py'
            }
        }

        stage('Archive data') {
            steps {
                archiveArtifacts artifacts: 'data.csv', onlyIfSuccessful: true
            }
        }
    }
}
