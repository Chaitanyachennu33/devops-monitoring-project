pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Chaitanyachennu33/devops-monitoring-project.git'
            }
        }

        stage('Check Ansible') {
            steps {
                sh 'which ansible || echo "ansible NOT found"'
                sh 'ansible --version || echo "cannot run ansible"'
            }
        }

        stage('Deploy') {
            steps {
                sh 'ansible-playbook -i inventory playbook.yml'
            }
        }
    }
}
