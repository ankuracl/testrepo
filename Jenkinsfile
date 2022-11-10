pipeline { 
agent any
    stages { 
        stage ('Build') { 
            steps {
                bat 'docker build -t testrepo:latest .'
            }
        } 
    } 
    post {
        always {
            bat 'docker logout'
        }
    }          
 }