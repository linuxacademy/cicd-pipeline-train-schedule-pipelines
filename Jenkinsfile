pipeline {
  agent any
  stage {
    stage ('Build') {
      steps {
        echo "Running Build Automation"
        sh './gradlew build -no-daemon'
        archiveArtifacts artifacts: 'dist/tarinSchedule.zip'
      }
    }
  }
}
