pipeline {
    agent {
        label 'AGENT-1'
    }
    options{
        timeout(time: 5, unit: 'SECONDS')
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo This is Build'
                sh 'sleep 10'
            }
        }
        stage('Test') {
            steps {
                sh 'echo This is Test'
            }
        }
        stage('Deploy') {
            steps {
                sh ' echo This is Deploy'
                // error 'Pipeline failed'
            }
        }
    }
}
post {
    always{
        echo  "This sections runs allways"
        deleteDir() // Deletes workspace contents
    }
    success{
        echo "This section run when pipeline sucess"
    }
    failure{
        echo "This section runs when pipeline failure"
    }
}