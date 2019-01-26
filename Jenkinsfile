pipeline {
    agent any
    parameters {
        choice(name: 'DEPLOY_ENV', choices: 'staging\nproduction', description: 'which deploy environment?')
    }
    stages {
        stage('Build') {
            steps {
                echo "Build ${params.DEPLOY_ENV}"
            }
        }
    }
}
