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
            emailext (to: 'tchambahorace3@gmail.com', body: 'test body', subject: 'test subject')
        }
    }
     
}




