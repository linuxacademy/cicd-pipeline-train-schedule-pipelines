pipeline{
   agent any
   
   stages{
  
  stage('Build'){
   
   echo 'Running Jenkins Automation'
   sh './gradlew Build --no-daemon'
  
  archiveArtifacts artifacts :'dist/trainSchedule.zip'
   }
   
   }
 
}
