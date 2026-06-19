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
            emailext (to: 'sergeshorace@yahoo.fr', body: 'test body', subject: 'test subject jenkins')
        }
    }
     
}




