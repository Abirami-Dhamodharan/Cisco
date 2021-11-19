pipeline {
    agent any

    stages {
        if (env.GIT_BRANCH == 'master') {
            stage('ecr-sync') {
            steps {
                echo 'Building..'
                sh 'printenv'
                echo env.BRANCH_NAME
                echo env.GIT_BRANCH
                def a = env.BRANCH_NAME ?: 'master'
                echo a
                echo env.USER
            }
        }
    }
}
}
