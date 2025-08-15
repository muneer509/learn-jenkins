pipeline {
    agent {
        label 'A1'
    }
    options{
        timeout(time: 60, unit: 'SECONDS')
        disableConcurrentBuilds()
    }
    parameters {
        string(name: 'ENVIRONMENT', defaultValue: 'dev', description: 'Environment to deploy to')
        booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Run tests before deployment?')
        choice(name: 'REGION', choices: ['us-east-1', 'us-west-2', 'eu-central-1'], description: 'AWS Region')
    }

    


    stages {
        stage('Build') {
           
              steps{
                
            sh 'echo Hello Build'
                // "echo This is build stage"          
              }
        }

        stage('test') {
        
              steps{
                
            sh 'echo Hello test'
                // "echo This is test stage"
              }
        }
    
stage('Approval') {
            steps {
                input message: 'Do you want to proceed?', ok: 'Yes'
            }
        }


    stage('Deploy') {
            
              steps{
                
            sh 'echo Hello deploy'
                // "echo This is Deploy stage"
            //     error 'pipeline failed'
            //   }
        }
    }
   
        stage('Print Parameters') {
            steps {
                echo "Environment: ${params.ENVIRONMENT}"
                echo "Run Tests: ${params.RUN_TESTS}"
                echo "Region: ${params.REGION}"
            }
        }
    
    }

post {
    always{
        echo "This section runs always"
        // DeleteDir()

    }
    success{
        echo "sucess"
    }
    failure{
        echo "failure"
    }
}
    }