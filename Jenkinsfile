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
                beforeInput true
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
