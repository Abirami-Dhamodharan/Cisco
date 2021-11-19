node() {
    stage('Checkout') {
        cleanWs notFailBuild: true
        checkout scm
        sh 'ls -lrth'
    }
}