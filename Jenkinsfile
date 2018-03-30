pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                call mvn clean package; 
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
