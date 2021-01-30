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
                echo "Building image-new"
                '''

            }
        }
        stage('Publish') {
            steps {
                sh '''
                 echo "make publish"
                '''
            }
        }
    }
}
