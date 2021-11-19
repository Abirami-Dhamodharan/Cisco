pipeline {
    agent any

    stages {
        stage('Check branch') {
            when { 
                    branch 'master'
            }
            steps {
                echo 'Building..'
            }
        }
    }
}
