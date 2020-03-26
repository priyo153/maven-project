pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                def mvnHome = tool 'M3'
                bat "${mvnHome}\\bin\\mvn clean PipelineAsCode"
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