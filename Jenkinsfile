pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                bat "mvnw clean PipelineAsCode"
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