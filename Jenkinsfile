pipeline{
  agent any
  tools{
  maven 'Maven'
  }
  
  stages{
  stage('Checkout'){
  steps{
    git branch:'master,url:'https://github.com/Disha-L12/lab1.git'
    }
  }
  stage('Build'){
  steps{
    sh 'mvn clean package'
    }
    }
  stage("test"){
  steps{
    sh 'mvn test'
    }
    }
    
 stage("run application"){
 steps{
   sh 'java -jar target/lab1-1.0-SNAPSHOT.jar'
   }
   }
 }
 post{
 success{
 echo "success"
 }
 failure{
 echo "failed"
 }
 }
 }
