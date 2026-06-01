pipeline {
    agent any

    environment {
        MY-VAR = 'one variable'
        MY-NUMBER = '123'
    }

    stages {
        stage('Build') {
            steps {
                echo "BRANCH_NAME: ${ env.BRANCH_NAME }"
                echo "BRANCH_IS_PRIMARY: ${ env.BRANCH_IS_PRIMARY }"
                echo "CI : ${ env.CI }"
                echo "BUILD_NUMBER : ${ env.BUILD_NUMBER }"
                echo "JENKINS-URL : ${ env.JENKINS_URL }"
                echo "MY-VAR : ${ env.MY-VAR }"
                echo "MY-NUMBER : ${ env.MY-NUMBER }"
                sh 'printenv'
            }
        }
    }
}