pipeline {
    agent {
        docker {
            image 'python:latest'
            args '-u root'
        }
    }

        stages {
        stage("install deps") {
            steps {
                sh 'pip install -r requirements.txt' 
                }
            }
        }
    }
}
