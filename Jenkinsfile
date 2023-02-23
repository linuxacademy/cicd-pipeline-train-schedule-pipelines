pipeline {
 agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello world!'
        echo 'Running build automation'
        // Define the API request data
        def api_url = 'http://127.0.0.1:8200/v1/ldap/static-role/learn'
        def api_token = 'root'
        def request_body = readFile 'data/learn-vault-ldap-role.json'
        
        // Make the API request with curl
        sh "curl -H 'X-Vault-Token: $api_token' -H 'Content-Type: application/json' -d '${request_body}' -s -X POST '${api_url}' > data/new-role.json"
        archiveArtifacts artifacts: 'dist/roleDetails.zip'
      }
    }
  }
}
