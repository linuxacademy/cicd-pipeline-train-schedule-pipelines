pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                echo 'Building source code...!' 
		sh './gradlew build --no-daemon'
		archiveArtifacts artifacts: 'dist/trainSchedule.zip', fingerprint: true
            }
        }
    }
}
