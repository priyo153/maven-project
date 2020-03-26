pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh 'mvn clean PipelineAsCode'
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