pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh ./gradlew build --no-daemon
                archiveArtifacts artifacts: 'dist/trainSchedule.zip',
                    allowEmptyArchive: true,
                    fingerprint: true,
                    onlyIfSuccessful: true
            } 
        }
    }
}
