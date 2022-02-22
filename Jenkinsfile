pipeline {
    agent any

    stages {
        stage('Build,_Gradle') {
            steps {
                echo 'Building..'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
    }
}