pipeline{
 agent any
 tools{
    maven 'Maven'
 
 
 stages{
   stage('checkout'){
     steps{
       git branch : 'main',url:'https://github.com/thrishaaaa/maven3.git'
     }
   }
   stage('Build'){
     steps{
       sh 'mvn clean package'
     }
   }
   stage('Test'){
     steps{
       sh 'mvn test'
     }
   }
   stage('Run Application'){
     steps{
       sh 'java -jar target/maven3-1.0-SNAPSHOT.jar'
     }
   }
 }
 post{
  success{
    echo 'build successful'
  }
  failure{
  echo 'failed'
  }
 }
 }
}
