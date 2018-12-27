pipeline {

    agent any
    stages {

        stage('Buiuld'){

            steps{
                sh 'mvn clean package'
            }
            post {
                success{
                    echo 'Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }

}