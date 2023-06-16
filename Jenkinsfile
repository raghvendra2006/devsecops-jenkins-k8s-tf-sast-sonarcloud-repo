pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=buggywebapp002 -Dsonar.organization=buggywebapp002 -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=59a7deca67268789983da4b436c23bc6e6517653'
			}
        } 
  }
}
