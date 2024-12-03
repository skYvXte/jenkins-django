pipeline {
    agent {
        docker {
            image 'python:latest'
            args '-u root'
        }
    }

        stages {
            stage("checkout"){
                steps{
                    git url: "${GIT_URL}",
                    branch: "${GIT_BRANCH}"
                }
            }
            stage("install deps") {
            steps {
                    sh 'pip install -r requirements.txt' 
                }
            }
            stage("test"){
                steps{
                    sh 'python manage.py test'
                }
            }
    }
}
