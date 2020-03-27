pipeline {
    agent any
     tools {
        maven 'localMaven'
    }
    stages{
        stage('Build'){
            steps {
                bat "mvn clean PipelineAsCode"
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