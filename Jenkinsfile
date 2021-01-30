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
                echo "Building image"
                '''

            }
        }
        stage('Deploy') {
            steps {
                sh 'make publish'
            }
        }
    }
}
