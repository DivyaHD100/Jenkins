pipeline {
    agent any
    environment { 
        ENV_URL = "pipelinelearning.com"
        SSH_CREDENTIALS = credentials('SSH_CRED')
    }
    stages{
                    stage('Parallel ') {
                    parallel {
                        stage('In Parallel 1') {
                            steps {
                                sh "cat /home/centos/file.txt"
                                echo "In Parallel 1"
                            }
                        }
                        stage('In Parallel 2') {
                            steps {
                                echo "In Parallel 2"
                            }
                        }
                    }
                }
        stage('stage -1'){
            steps {
                sh "echo 1st stage $ENV_URL"
                sh "env"
            }


        }
         stage('stage -2'){
             when {branch 'dev'}
            steps {
                sh "echo 2nd stage"
            }


        }
         stage('final stage:needs attention'){
             input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                }
             }
            steps {
                sh "echo 3rd stage"
            }


        }

    }
}

 