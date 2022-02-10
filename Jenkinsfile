pipeline {
  agent any
  stages {
    stage('Hello') {
      steps {
        script {
          if (env.BRANCH_NAME == 'develop') {
		 echo "Hello from jenkinsfile_dev" 
                 stage('Prepare Deployment') {
		   steps{
                     sh '''
			echo "Stage1 and Step1 in development"
			'''
                     }
		}
	}
          else if (env.BRANCH_NAME == 'uat') {
		echo "Hello from jenkinsfile_uat" 
		stage('Prepare Deployment') {
                   steps{
                     sh '''
                        echo "Stage1 and Step1 in uat"
                        '''
                     }
		}
	}	
          else if (env.BRANCH_NAME == 'master') {
		echo "Hello from jenkinsfile_master" 
		stage('Prepare Deployment') {
                   steps{
                     sh '''
                        echo "Stage1 and Step1 in master"
                        '''
                     }
		}
	}
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
