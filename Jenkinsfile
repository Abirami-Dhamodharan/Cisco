node() 
    if (env.BRANCH_NAME == 'master') {

        stage('checkout') {
            cleanWs notFailBuild: true
            checkout scm
            sh 'ls -lrth'
        }

        stage('ecr-sync') {
            script {
                def projects = readJSON file:'cmc.json'
            }
        }
    }    
}