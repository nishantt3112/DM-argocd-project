

pipeline {
    agent {
        label 'build-agent'
    }

    tools {
        jdk 'java17'
        maven 'maven3'
    }

    stages{
        stage('cleanWorkspace')
            steps{
                cleanWs()
            }
    }

    stages{
        stage('codeCheckout'){
            steps{
                git branch: 'main', credentialsId: 'github-1', url: 'https://github.com/nishantt3112/DM-argocd-project.git'
            }
        }
    }

}