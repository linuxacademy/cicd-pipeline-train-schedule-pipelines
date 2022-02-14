pipeline {
    agent any
    stages {
        stage('Tag and Push') {
            environment {
		GIT_TAG = "GG-${BUILD_NUMBER}"
	        }
	    when {
                expression { return params.current_status == "closed" && params.merged == true }
            }
            steps {
                withCredentials([usernamePassword(credentialsId: 'github_creds', passwordVariable: 'GIT_PASS', usernameVariable: 'GIT_USER')]) {
		sh('''
		 	git config --global user.email "tauanov.aidos@gmail.com"
			git config --global user.name  "altynbai"
			git config --global push.default matching
			git tag -a $GIT_TAG -m "[Jenkins CI] New Tag"
			git push https://$GIT_USER:$GIT_PASS@github.com/altynbai/cicd-pipeline-train-schedule-pipelines.git $GIT_TAG
		''')
                }
            }
        } 
    }
}
