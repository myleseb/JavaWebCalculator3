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
                ansiblePlaybook credentialsId: 'centosnode1keygn', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'src', playbook: 'apache.yml', vaultTmpPath: ''
            }
        }
    }
}
