pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                script {
                  git branch: 'main', credentialsId: 'github_credential', url: 'git@github.com:omeshvalyal/ansible-job.git'
                }
            }
        }

        // Add more stages as needed for your build, test, and deployment steps
        stage('Build') {
            steps {
                echo 'Build your code here'
                // Add your build steps
            }
        }

        stage('Test') {
            steps {
                echo 'Run tests here'
                // Add your test steps
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy your application'
                // Add your deployment steps
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
