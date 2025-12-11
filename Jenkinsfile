pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning the repository'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                sh 'pytest'
            }
        }

        stage('Build Artifact') {
            steps {
                sh 'zip build.zip app.py'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying artifact...'
            }
        }
    }
}
