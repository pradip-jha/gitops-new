pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Pull') {
            steps {
                sh 'ls -l'
            }
        }
        stage('Build'){
            steps {
                sh '''
                env
                echo "Building image-new"
                docker build flask-app/ -t pankaj2934/flask-gitops:"${BUILD_NUMBER}"
                '''

            }
        }
        stage('Publish') {
            steps {
                sh '''
                 docker push pankaj2934/flask-gitops:"${BUILD_NUMBER}"
                '''
            }
        }
    }
}
