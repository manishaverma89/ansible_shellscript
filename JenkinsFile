pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'ansibleshellscript', credentialsId: 'ManishaGitHub', url: 'https://github.com/manishaverma89/ansible_shellscript.git'
            }
        }
        stage('Execute Ansible') {
            steps {
                ansiblePlaybook disableHostKeyChecking: true, installation: 'Ansible', playbook: 'helloscript.yml'
            }
        }
    }
}
