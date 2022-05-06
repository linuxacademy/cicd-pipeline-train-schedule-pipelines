pipeline {
  agent any
  stages {
    stage{"build") {
      steps {
        sh ./gradlew build --no-daemon
        archiveArtifacts artfacts: 'dist/trainSchedule.zip'
      }
    }    
  }
}
