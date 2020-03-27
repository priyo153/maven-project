pipeline {
    agent any
     tools {
        maven 'localMaven'
    }
    stages{
        stage('Build'){
            steps {
                cmd_exec( "mvn clean PipelineAsCode")
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