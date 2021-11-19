pipeline {
    agent any

    stages {
        stage('ecr-sync') {
            when { 
                    branch 'master'
            }
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
