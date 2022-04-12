pipeline{
agent any
  stages{
    stage("build){
          steps{
            echo "hello world"
          sh echo "hello"
            sh './gradlew build --no-daemon
            archiveArtifacts artifacts:'dist/trainSchedule.zip'
          }
        
          
          }
  }
}
