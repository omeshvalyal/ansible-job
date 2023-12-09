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
                    // Replace 'your-playbook.yml' with the actual name of your Ansible playbook
                    ansiblePlaybook(
                        playbook: '/home/ansible/my_play/start-tom.yaml',
                        inventory: '/etc/ansible/hosts'
                    )
                }
            }
        }
    }
}
