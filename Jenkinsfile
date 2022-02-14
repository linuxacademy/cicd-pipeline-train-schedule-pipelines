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
                sh('''
		 	git config --global user.email "tauanov.aidos@gmail.com"
			git config --global user.name  "altynbai"
			git config --global push.default matching
			git tag -a $GIT_TAG -m "[Jenkins CI] New Tag"
			git push https://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@github.com/altynbai/cicd-pipeline-train-schedule-pipelines.git $GIT_TAG
		''')
               
            }
        } 
    }
}
