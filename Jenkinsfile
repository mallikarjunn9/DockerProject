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
               ansiblePlaybook installation: 'ansible', inventory: '/var/lib/jenkins/project/hosts', playbook: '/var/lib/jenkins/project/docker.yml', sudoUser: 'jenkins'
            }
        }
    }
}
