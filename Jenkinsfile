node {
   
   stage('Code Checkout') { // for display purposes
      git url: 'https://github.com/itrainarticle370/maven-examples.git'
   }
   stage('Build') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.0') {
     sh 'mvn clean compile'
     } 
   }
   stage('UnitTest run') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.0') {
     sh 'mvn test'
     }   
   }
   stage('Code Quality') {
     withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.0') {
     sh 'mvn sonar:sonar \
  -Dsonar.projectKey=admin-raja \
  -Dsonar.organization=admin-raja \
  -Dsonar.host.url=https://sonarcloud.io \
  -Dsonar.login=b67af65b46da10c1b38ff5e1394953\
     }    
      
   }
   stage('Archival repo') {
    withMaven(jdk: 'JDK-1.8', maven: 'Maven-3.6.0') {
     sh 'mvn package'
     }   
   }
   stage('Docker Build') {
      
   }
   stage('Deploy to Prod') {
      
   }
   
}
