pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                call mvn clean install; 
				call mvn   }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
