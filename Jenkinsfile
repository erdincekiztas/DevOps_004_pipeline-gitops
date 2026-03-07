pipeline {
    agent {
        node {
            label 'My-Jenkins-Agent'
        }
    }

    environment {
          APP_NAME = "devops-application-gitops"
    }



    stages {

        stage('Clean Workspace') {
                steps {
                cleanWs()
            }
        }

        stage('SCM GitHub') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/erdincekiztas/devops_004_pipeline-gitops']])
            }
        }

      


  // Deployment kısmında güncelleme


  // Yapılan güncellemeyi de  GitHub'a göndereceğiz.



    }
}