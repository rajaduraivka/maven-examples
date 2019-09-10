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
        -Dsonar.projectKey=article370-maven \
        -Dsonar.organization=article370 \
        -Dsonar.host.url=https://sonarcloud.io \
        -Dsonar.login=cd592244616035dc27e5e749283e855c44c3eecf'
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
