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
                echo env.USER
            }
        }
    }
}
