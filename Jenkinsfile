pipeline {
    agent any

    stages {
        stage('Build') {
            
            steps {
                echo 'hello'
            }
        }  
    }   

    post {
        success {
            emailext (to: 'sergeshorace@yahoo.fr', body: '$DEFAULT_CONTENT', subject: '$DEFAULT_SUBJECT')
        }
    }
     
}




