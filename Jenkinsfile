pipeline {
    agent any
    tools{
        maven 'local maven'
    }
    stages{
        stage ('build'){
            steps{
                sh 'mvn clean package'
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
