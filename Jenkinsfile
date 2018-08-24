pipeline {
agent any
stages {
stage ('BUild')
            {
             steps
                        {
            {
                  echo 'Running Build automation'
                   sh './gradlew build' --no-daemon'
                   archiveArtifacts artifacts 'dist/trainSchedule.zip'
            }  
                        }
        }
                        
      }
