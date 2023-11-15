pipeline{
    agent any
    stages{
        stage('Git Checkout'){
            steps{
                git 'https://github.com/myleseb/JavaWebCalculator3.git'
            }
        }
        
        stage('Run Ansible Script'){
            steps{
ansiblePlaybook credentialsId: 'pkey', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'host.init', playbook: 'apache.yml', vaultTmpPath: ''       }
        }
    }
}
