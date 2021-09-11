pipeline {
  agent any 
  stages { 
     stage("build") { 
        steps { 
            echo " running build automating " 
            sh './gradlew build --no-daemon'
            archiveArtifacs artifacts : 'dist/trainSchedule.zip'
        }
     }
  }
}
