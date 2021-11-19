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
                env.GIT_BRANCH = env.BRANCH_NAME ?: 'master'
                echo env.GIT_BRANCH
                echo env.USER
            }
        }
    }
}
