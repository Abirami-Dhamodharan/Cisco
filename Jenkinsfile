pipeline {
    agent any

    stages {
        stage('Check branch') {
            when {
                not { 
                    branch 'master'
                }
            }
            steps {
                echo 'Building..'
            }
        }
    }
}
