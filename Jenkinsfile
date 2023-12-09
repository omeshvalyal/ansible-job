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
 stage('Execute Ansible Playbook') {
            steps {
                script {
                    ansible-playbook myfile.yaml
                }
            }
        }
    }
}
