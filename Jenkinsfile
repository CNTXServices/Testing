#!groovy
pipeline {
  agent any
  stages {
    stage('build code') {
      steps {
	dir('edge') {
          script {
            if (env.BRANCH_NAME == 'develop') {
            //  echo "Hello from jenkinsfile_dev" 
                    sh '''
			pwd
                        echo "Stage1 and Step1 in development branch"
                    '''
                    }
        
            else if (env.BRANCH_NAME == 'uat') {
            // echo "Hello from jenkinsfile_uat" 
                    sh '''
			pwd
                        echo "Stage1 and Step1 in uat branch"
                    '''
                    }
            else if (env.BRANCH_NAME == 'master') {
            // echo "Hello from jenkinsfile_master" 
                    sh '''
			pwd
                        echo "Stage1 and Step1 in master"
                    '''
                    }
            else {
                exit 0
                echo "Incorrect branch" 
                }
            }
        }
    }
}
    stage('deploy code') {
      steps {
        println "deploy code to target servers"
        script {
            if (env.BRANCH_NAME == 'develop') {
                sh '''
                    echo "deploying code in development"
                '''
            }
            else if (env.BRANCH_NAME == 'uat') {
                sh '''
                echo "deploying code in uat"
                '''
            }
            else if (env.BRANCH_NAME == 'master') {
                sh '''
                echo "deploying code in  master"
                '''
            }
            else {
                sh '''
                echo "Incorrect branch"
                exit 0
                ''' 
               }
            }
         }
      }
   }
}
