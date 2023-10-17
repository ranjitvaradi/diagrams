pipeline {
  agent any

  environment {
    deploymentName = “diagrams_deployment”
    containerName = "diagrams-container"
    serviceName = “diagrams-svc"
    imageName = "nginxdemos/hello"
  }

  stages {

    stage('Build Artifact - Maven') {
      steps {
        sh "mvn clean package -DskipTests=true"
        archive 'target/*.jar'
      }
    }

    stage('Unit Tests - JUnit and JaCoCo') {
      steps {
        sh "mvn test"
      }
    }

    
   
    
    
  
}
