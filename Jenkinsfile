pipeline {
    agent any
    tools{
        maven 'local maven'
    }
    stages{
        stage('build'){
            steps{
                bat 'mvn clean package'
            }
            post {
                success {
                    echo '开始i存档...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
