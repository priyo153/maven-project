pipeline {
    agent any
     tools {
        maven 'localMaven'
    }
    stages{
        stage('Build'){
            steps {
                bat "mvn clean"
            }
            post {
                success {
                    echo 'Now Archiving in progress...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}