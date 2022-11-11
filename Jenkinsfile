pipeline { 
agent any
    stages { 
        stage ('Build') { 
            steps {
                sh 'docker build -t testrepo:latest .'
            }
        } 
    } 
    post {
        always {
            sh 'docker logout'
        }
    }          
 }
