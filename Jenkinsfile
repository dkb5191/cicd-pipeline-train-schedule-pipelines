pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh "
                    ./gradlew build --no-daemon
                "
            }
    }

    post {
        always {
            archiveArtifacts artifacts: 'dist/trainSchedule.zip'
        }
    }
}