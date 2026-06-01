pipeline {
    agent {
        docker{
            image 'node:24-alpine'
        }
    }

    stages {
        stage('Build') {
            steps {
                sh 'npm -V'
            }
        }
    }

    post{
        always {
            echo ' always run !'
        }
        success {
            echo ' success run !'
        }
    }
}



