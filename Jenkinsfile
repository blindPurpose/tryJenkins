pipeline {
  agent any
  stages {
    stage('Build Application') { 
      steps {
        bat 'mvn clean install'
      }
    }
 	stage('Test') { 
      steps {
        echo 'Test Appplication...' 
        bat 'mvn test'
      }
    }
	stage('Deploy') { 
        steps {
        echo 'Deploying only because of code commit...'
        echo " deploying to Sandbox environent"
       
        bat 'mvn package deploy -DmuleDeploy'
      }
    }
 	
	
  }
}
