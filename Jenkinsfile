pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                sh 'rm -rf prometheus'
                sh 'git clone https://github.com/Soumya12346/prometheus.git'
            }
        }
        stage('Deploy Prometheus') {
            steps {
                sh 'ansible-playbook prometheus.yml -i inventory/hosts'
            }
        }
    }
}
