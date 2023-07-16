pipeline {
    agent any
    
    stages {
        stage('checkout') {
            steps{
                git branch: "main",
                    credentialsId:'jenkins-user-yc',
                    url: 'git@github.com:nakhush/ansible-deploy.git'
                    
                //checkout([$class: 'GitSCM'], branches: [[ name: '*/main' ]], userRomoteConfig: [[credentialsID: 'jenkins-user-yc']], url: 'git@github.com:nakhush/ansible-deploy.git')
                sh "ls -la"
            }
        }
        stage('deploy') {
            steps{
                sh "ansible-playbook playbook.yml"
            }
        }
    }    
}
