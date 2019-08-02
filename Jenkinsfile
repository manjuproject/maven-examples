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
