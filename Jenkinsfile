pipeline {
    agent any
    parameters {
        choice(name: 'DEPLOY_ENV', choices: 'staging\nproduction', description: 'which deploy environment?')
        text(name: 'BIOGRAPHY', description: 'Enter some information about the person')
    }
    stages {
        stage('Build') {
            steps {
                echo "Build ${params.DEPLOY_ENV}"
            }
        }
    }
}
