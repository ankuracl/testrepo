pipeline { 
agent any
    environment {
        IMAGE_NAME = 'testrepo'
        IMAGE_TAG = 'latest'
    }
    stages { 
        stage ('Build') { 
            steps {
                bat 'docker build -t $IMAGE_NAME:$IMAGE_TAG .'
            }
        } 
    } 
    post {
        always {
            bat 'docker logout'
        }
    }          
 }