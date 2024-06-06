pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
               checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '697b1403-666a-4d37-99ca-c90b4150df32', url: 'https://github.com/ankurjha21/ansible-beginner']]])
            }
        }
        stage('Execute Ansible playbook') {
            steps {
                ansiblePlaybook playbook: 'playbook.yaml'
            }
        }
    }
}
