pipeline {
    agent {
        label 'A1'
    }
    options{
        timeout(time: 60, unit: 'SECONDS')
        disableConcurrentBuilds()
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
    

    stage('Deploy') {
            
              steps{
                
            sh 'echo Hello deploy'
                // "echo This is Deploy stage"
            //     error 'pipeline failed'
            //   }
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