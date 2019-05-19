pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
        }
        post {
            succes {
                echo 'Now Archiving...'
                archiveArtifacts artifacts: '**/*.war'
            }
        }
    }
}
}
