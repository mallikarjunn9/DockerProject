pipeline {
    agent any
    stages{
        stage('Git Checkout'){
            steps {
                git "https://github.com/mallikarjunn9/DockerProject.git"
            }
        }
        stage('Execute Ansible'){
            steps {
                ansiblePlaybooksh disableHostkeyChecking: true, installation:'ansible2', inventory: 'dev.inv', playbook:'apache.yml'
            }
        }
    }
}
