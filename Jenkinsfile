pipeline {
  
  agent any

  tools {
      maven 'M3'
  }

  stages {
  
      stage("Pull"){
        checkout scm
      }

      stage("build"){
        sh "mvn clean verify -DskipITs=true"
        echo "${BUILD_NUMBER}"
        sh 'ls -l'
       }
       stage("report"){
           junit '**/target/surefire-reports/TEST-*.xml'
       }
       stage("archive"){
           archive 'target/*.war'
       }
    }

}
