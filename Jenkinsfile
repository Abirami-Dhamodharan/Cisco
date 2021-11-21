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
                echo projects['subServices'][0]
                echo projects['subServices'][0]['packages'][0]['version']
            }
        }  
}