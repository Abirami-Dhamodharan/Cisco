pipeline {
    agent any

    stages {
        stage('ecr-sync') {
            when { 
                    branch 'master'
            }
            steps {
                echo 'Building..'
                echo '$BRANCH_NAME'
            }
        }
    }
}
