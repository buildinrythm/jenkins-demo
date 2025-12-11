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
                sh '/usr/bin/pip3 install --upgrade pip'
                sh '/usr/bin/pip3 install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                sh '/usr/bin/python3 -m pytest'
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
