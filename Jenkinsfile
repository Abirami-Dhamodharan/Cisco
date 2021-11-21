node() {
        echo env.BRANCH_NAME 

        stage('checkout') {
            cleanWs notFailBuild: true
            checkout scm
            sh 'ls -lrth'
        }

        stage('ecr-sync') {
            script {
                def projects = readJSON file:'cmc.json'
                echo projects['service']['status']
            }
        }  
}