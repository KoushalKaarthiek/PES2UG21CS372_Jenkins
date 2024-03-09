pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building'
                build 'PES2UG21CS372-1'
                sh 'g++ main2.cpp -o output'
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
