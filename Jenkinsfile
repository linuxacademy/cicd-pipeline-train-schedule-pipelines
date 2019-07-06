pipeline {
agent any
stages {
stage ('build') {
steps {
echo 'Running build automation from jenkins file'
sh './gradlew build --no-daemon'
archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
