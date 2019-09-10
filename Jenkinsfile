node {
   
   stage('Code Checkout') { // for display purposes
git credentialsId: 'e6a569b9-a163-4720-8edf-fd7afc32a6a0', url: 'https://github.com/rajaduraivka/maven-examples.git' 
   }
   
   stage('Build') {
    withMaven(jdk: 'JDK-2.00', maven: 'Maven-3.6.0') {
     sh 'mvn clean compile'
     } 
   }
   stage('UnitTest run') {
    withMaven(jdk: 'JDK-2.00', maven: 'Maven-3.6.0') {
     sh 'mvn test'
     }   
   }
   stage('Code Quality') {
     withMaven(jdk: 'JDK-2.00', maven: 'Maven-3.6.0') {
   
     }    
      
   }
   stage('Archival repo') {
    withMaven(jdk: 'JDK-2.00', maven: 'Maven-3.6.0') {
     sh 'mvn package'
     }   
   }
   stage('Docker Build') {
      
   }
   stage('Deploy to Prod') {
      
   }
   
}
