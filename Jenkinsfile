pipeline {
    agent any
    environment { 
        ENV_URL = "pipelinelearning.com"
    }
    stages{
        stage ('stage -1'){
            steps {
                sh "echo 1st stage $ENV_URL"
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
 