pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building'
                build 'PES2UG21CS372-1'
                sh 'g++ New.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing'
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
                echo 'Deployed'
            }
        }
    }

    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
