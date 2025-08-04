pipeline {
    agent {
        label 'AGENT-1'
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo This is Build'
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
                error 'Pipeline failed'
            }
        }
    }
}
post {
    always{
        echo  "This sections runs allways"
    }
    success{
        echo "This section run when pipeline sucess"
    }
    failure{
        echo "This section runs when pipeline failure"
    }
}