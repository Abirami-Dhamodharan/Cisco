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
                def tag = projects['subServices'][0]['packages'][0]['version'] + '-' + projects['subServices'][0]['packages'][0]['build']
                echo tag
            }
        }  
}