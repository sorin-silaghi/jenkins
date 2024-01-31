pipeline {
    agent any

    parameters {
        choice(name: 'DEPLOY_PARAM_ENV', choices: ['none', 'dev', 'demo', 'prod'], description: 'Pick the environment you want to deploy to. Use none if you don\'t want to deploy anywhere')
        booleanParam(name: 'CLEAR_DB', defaultValue: false, description: 'Clear the environment DB before deployment')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building.. ${DEPLOY_PARAM_ENV}'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
