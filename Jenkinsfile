pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                sh 'rm -rf prometheus'
                sh 'git clone https://github.com/sanjay0288/prometheus.git'
            }
        }
        stage('Deploy Prometheus') {
            steps {
                sh 'sudo ansible-playbook prometheus.yml -i inventory/hosts'
            }
        }
    }
}
