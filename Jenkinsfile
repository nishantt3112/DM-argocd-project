

pipeline{
    agent{
         label 'build-agent'
    }

    tools{
        jdk 'java 17'
        maven 'maven3'
    }

    stages{
        stage('cleanWorkspace'){
            steps{
                cleanWs()
            }
        }


        stage('codeCheckout'){
            steps{
                git branch: 'main', credentialsId: 'github-1', url: 'https://github.com/nishantt3112/DM-argocd-project.git'
            }
        }

        stage('codeBuild'){
            steps{
                sh 'mvn clean package'
            }
        }
     
        stage('codeTest'){
            steps{
                sh 'mvn test'
            }
        }
    }

}