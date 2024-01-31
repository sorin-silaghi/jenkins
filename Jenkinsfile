pipeline {
    agent any

    parameters {
        choice(name: 'DEPLOY_PARAM_ENV', choices: ['none', 'demo', 'prod'], description: 'Pick the environment you want to deploy to. Use none if you don\'t want to deploy anywhere')
        booleanParam(name: 'CLEAR_DB', defaultValue: false, description: 'Clear the environment DB before deployment')
    }
    environment {
      BRANCH_NAME = '${params.DEPLOY_PARAM_ENV}'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building.. ${BRANCH_NAME}'
                sh 'printenv'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            when {
              expression { BRANCH_NAME ==~ /(none)/ || params.DEPLOY_PARAM_ENV ==~ /(demo|prod)/  }
            }
            steps {
                echo 'Deploying....'
            }
        }
    }
}
