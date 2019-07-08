pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo 'Running a shell script'
                sh './gradlew build --no-daemon'
                
            }
        }
    }
  post {
        always {
            archiveArtifacts artifacts: 'dist/trainSchedule.Zip', fingerprint: true
        }
    }
}
