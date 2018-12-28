pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                echo 'Building source code...!' 
		sh './gradlew build'
		archiveArtifacts artifacts: 'dist/trainSchedule.zip', fingerprint: true
            }
        }
    }
}
