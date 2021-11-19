pipeline {
    agent any

    stages {
        stage('ecr-sync') {
            when { 
                allOf{
                    branch 'master'
                    equals(actual:env.USER,expected:'adhamodh')
                }
            }
            steps {
                echo 'Building..'
                sh 'printenv'
                echo env.BRANCH_NAME
                echo env.GIT_BRANCH
                echo env.USER
                
            }
            steps {
                def props = readJSON file: 'cmc.json'
                echo props['service']['status']
            }
        }
    }
}
