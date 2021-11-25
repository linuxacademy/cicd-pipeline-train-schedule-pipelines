
pipeline {
  agent any
    stages {
      stage ('Build') {
        steps {
          echo 'Running build automation'
          sh ' ./gradle build --no-daemon'
          archive artifacts: 'dist/trainSchedule'
        }
      }
      stage ('2-Test') {
        steps {
          echo "Starting test automation"
          echo 'Running test automation'
          echo 'Ending test automation'

        }
      }
      stage('3-Deplo') {
        steps {
          echo "Starting deployment automation"
          echo 'Running deployment automation'
          echo 'Ending deployment automation'

        }
      }
    }
  }
