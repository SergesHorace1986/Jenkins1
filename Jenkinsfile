pipeline {
    agent any
    
    parameters {
        string(name: 'NAME', defaultValue: 'Jenkins', description: 'Who are me?')
        text(name: 'TEXT', defaultValue: 'a text', description: 'Provide a description')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'true or false')
        choice(name: 'CHOICE', choices: ['Development', 'Testing', 'Production'], description: 'Select the environment')
        password(name: 'API_KEY', description: 'Enter your API key')
    }

    triggers {
        pollSCM('* * * * *') // Schedule to run at 4 AM on weekdays
    }

    stages {
        stage('Build') {
            
            steps {
                echo "Hello, ${params.NAME}!"
                echo "Text: ${params.TEXT}"
                echo "Toggle: ${params.TOGGLE}"
                echo "Choice: ${params.CHOICE}"
                // Note: Avoid printing sensitive information like API keys in real scenarios
                echo "API Key: ${params.API_KEY}"
            }
        }

        stage('Deployment - Production') {
            input {
                message "Do you want to deploy to production?"
                ok "Deploy"
                submitter "admin,devops"
                submitterParameter "USER_SUBMIT"
                parameters {
                    string(name: 'VERSION', defaultValue: 'latest', description: 'Version to deploy')
                }
            }
            steps {
                echo "USER : ${ USER_SUBMIT }"
                echo "version : ${ VERSION}"
                echo 'Deploying to production...'
            }
        }
    }    
}



