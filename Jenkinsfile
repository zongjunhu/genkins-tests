pipeline {
  
  agent any

  tools {
      maven 'M3'
  }

  stages {
  
      stage("Pull"){
          steps {
            checkout scm
          }
      }

      stage("build"){
          steps {
            maven "clean verify -DskipITs=true"
            echo "${BUILD_NUMBER}"
            sh 'ls -l'
          }
       }
       stage("report"){
          steps {
           junit '**/target/surefire-reports/TEST-*.xml'
          }
       }
       stage("archive"){
          steps {
           archive 'target/*.war'
          }
       }
    }

}
