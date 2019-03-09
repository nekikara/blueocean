pipeline {
    agent any
    stages {
        stage('all') {
            steps {
                echo 'node -v'
            }
        }
        stage('deploy') {
            when {
                branch 'deploy'
            }
            steps {
                input {
                    message "Should we continue?"
                    ok "Yes, we should."
                    submitter "alice,bob"
                    parameters {
                        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                    }
                }
                echo "Hello, ${PERSON}, nice to meet you."
            }
        }
    }
}
