pipeline {
    agent {
        docker {
            image 'node:8-jessie'
        }
    }
    stages {
        stage('deploy') {
            when {
                branch 'deploy'
            }
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                }
            }
            steps {
                echo "Hello, ${PERSON}, nice to meet you."
            }
        }
    }
}
