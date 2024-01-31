pipeline {
    agent any

    parameters {
        choice(name: 'DeploymentEnv', choices: ['none', 'dev', 'demo', 'prod'], description: 'Pick the environment you want to deploy to')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building.. ${params.DeploymentEnv}'
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
