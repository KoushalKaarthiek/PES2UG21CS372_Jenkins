pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'echo "building"'
                build 'PES2UG21CS372'
                sh 'g++ New.cpp -o output'
            }
        }
        stage('Test') { 
            steps {
                sh 'echo "testing"'
                sh './output'

            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo "deploying"' 
                sh 'echo "deployed"'
            }
        }
    }
    post{
        failure{
            error 'pipeline failed'
        }
    }
}
}
