pipeline {
    agent any
    environment { 
        ENV_URL = "pipelinelearning.com"
        SSH_CREDENTIALS = credentials('SSH_CRED')
    }
    stages{
        stage ('stage -1'){
            steps {
                sh "echo 1st stage $ENV_URL"
                sh "env"
            }


        }
         stage ('stage -2'){
            steps {
                sh "echo 2nd stage"
            }


        }
         stage ('stage -3'){
            steps {
                sh "echo 3rd stage"
            }


        }

    }
}
 