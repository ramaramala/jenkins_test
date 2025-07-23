pipeline {
    agent {
        docker {
            image 'python:3.10-slim'
        }
    }
    stages {
        stage('Install Dependencies') {
            steps {
                sh 'pip install flask'
            }
        }

        stage('Run Flask App') {
            steps {
                sh 'python app.py &'
                sh 'sleep 5'
                sh 'curl http://localhost:5000'
            }
        }
    }
}
