node() {
    if (env.BRANCH_NAME == 'master') {
        stage('Checkout') {
            cleanWs notFailBuild: true
            checkout scm
            sh 'ls -lrth'
        }
    }    
}