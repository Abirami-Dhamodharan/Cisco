pipeline {
    agent any

    stages {

        stage('Setup parameters') {
            steps {
                script { 
                    properties([
                        parameters([
                            string(
                                name: 'TAG', 
                                description: 'Tag of antares image',
                                defaultValue: 'latest',
                                trim: true
                            ),
                            string(
                                name: 'SPARKROOMID', 
                                description: 'Spark Room ID to post notification message',
                                defaultValue: 'latest',
                                trim: true
                            )
                        ])    
                    ])
                
                }
            }
        }

        stage('Checkout') {
            steps {
                cleanWs notFailBuild: true
                checkout scm
                sh 'ls -lrth'
            }    
        }

        stage('Build') {
            steps {
                echo 'Building..'
                echo params.TAG
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
