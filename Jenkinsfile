pipeline {
    agent any
    stages {
        stage('all') {
            steps {
                echo 'node -v'
            }
        }
        stage('deploy') {
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
                parameters {
                    choice(name: 'DEPLOY_STAGE', choices: ['production', 'staging'], description: 'Who should I say hello to?')
                }
            }
            steps {
                echo "deploy to ${params.DEPLOY_STAGE}"
            }
        }
    }
}
