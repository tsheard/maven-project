pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                mvn clean install; 
				}
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
