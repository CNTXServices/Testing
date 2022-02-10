pipeline {
  agent any
  stages {
    stage('Hello') {
      steps {
        script {
          if (env.BRANCH_NAME == 'develop') {
		 echo "Hello from jenkinsfile_dev" }
          else if (env.BRANCH_NAME == 'uat') {
		echo "Hello from jenkinsfile_uat" }
          else if (env.BRANCH_NAME == 'master') {
		echo "Hello from jenkinsfile_master" }
	  else {
		echo "Incorrect branch" }
            }
        }
    }
    stage('Hello_01') {
      steps {
        echo "Hello for testing 1"
            }
        }

    }
}
