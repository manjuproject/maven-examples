node {
   
   stage('Code Checkout') { 
   git credentialsId: 'githubid', url: 'https://github.com/manjuproject/maven-examples.git'     
    }
   stage('Build') {
    withMaven(jdk: 'jdk-8', maven: 'MAVEN') {
      sh 'mvn clean compile'
      }
    }
   stage('Unit Test run') {
    withMaven(jdk: 'jdk-8', maven: 'MAVEN') {
     sh 'mvn test'
      } 
    }
   stage('sonarqube'){
      withMaven(jdk: 'jdk-8', maven: 'MAVEN') {
         sh 'mvn sonar:sonar -Dsonar.projectKey=maven-examp -Dsonar.organization=manjuproject -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=21f657b170c7eba8698b097526446188d32735aa'    
         
      }
   }
 
   stage('Package to Jfrog') {
    withMaven(jdk: 'jdk-8', maven: 'MAVEN') {
     sh 'mvn package'
      }
    }
   
   stage('Deploy to Dev') {
     
    }
   stage('Automation Testing') {
     
    }
   stage('Deploy to Test') {
     
    }
   stage('Smoke Testing') {
     
    }
   stage('Deploy to Prod') {
     
    }
   stage('Acceptance Testing') {
     
    }
}
