pipeline {
    agent any
    stages {
        stage('Build') {
           
              steps{
                
            bat 'echo Hello Build'
                // "echo This is build stage"
              }
        }

        stage('test') {
        
              steps{
                
            bat 'echo Hello test'
                // "echo This is test stage"
              }
        }
    

    stage('Deploy') {
            
              steps{
                
            bat 'echo Hello deploy'
                // "echo This is Deploy stage"
            //     error 'pipeline failed'
            //   }
        }
}
post {
    always{
        echo "This section runs always"
    }
    success{
        echo "sucess"
    }
    failure{
        echo "failure"
    }
}
        }
}