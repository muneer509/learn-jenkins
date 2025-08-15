pipeline {
    agent {
        label 'A1'
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
        
          script {
                // Delete the current build
                def job = Jenkins.instance.getItemByFullName(env.JOB_NAME)
                job.getBuildByNumber(env.BUILD_NUMBER)?.delete()
            }

    }
    success{
        echo "sucess"
    }
    failure{
        echo "failure"
    }
}
    }