pipeline {
  agent any 
  stages {
    stage ('Build') {
      steps {
      echo "running build"
      sh ./gradlew build --no-daemon
      archiveArtifacts :"dist/trainSchedule.zip"
      }
    }
  }
}
    
