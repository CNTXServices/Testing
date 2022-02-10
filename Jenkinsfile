#!groovy
pipeline {
  agent any
  stages {
    stage('build code') {
      steps {
        script {
            if (env.BRANCH_NAME == 'develop') {
            //  echo "Hello from jenkinsfile_dev" 
                    sh '''
                        echo "Stage1 and Step1 in development"
                    '''
                    }
        
            else if (env.BRANCH_NAME == 'uat') {
            // echo "Hello from jenkinsfile_uat" 
                    sh '''
                        echo "Stage1 and Step1 in uat"
                    '''
                    }
            else if (env.BRANCH_NAME == 'master') {
            // echo "Hello from jenkinsfile_master" 
                    sh '''
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
    stage('deploy code') {
      steps {
        println "deploy code to taget servers"
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
