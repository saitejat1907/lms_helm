pipeline {
    agent any

    stages {
        stage("Installing Kubernetes Module") {
            steps {
                ansiblePlaybook credentialsId: 'Ansible',
                                 disableHostKeyChecking: true,
                                 installation: 'Ansible',
                                 inventory: 'dev.inv',
                                 playbook: 'playbook/sync-helm-chart.yml'
            }
        }
}
