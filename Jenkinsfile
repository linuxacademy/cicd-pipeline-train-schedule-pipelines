pipeline {
agent any
stages {
stage ('BUild')
            {
                  echo 'Running Build automation'
                   sh './gradlew build' --no-daemon'
                   archiveArtifacts artifacts 'dist/trainSchedule.zip'
            }    
        }
      }
