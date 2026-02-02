pipeline {
    agent any
stage('Check Ansible') {
    steps {
        sh 'which ansible || echo "ansible NOT found"'
        sh 'ansible --version || echo "cannot run ansible"'
    }
}

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Chaitanyachennu33/devops-monitoring-project.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh 'ansible-playbook -i inventory playbook.yml'
            }
        }
    }
}
