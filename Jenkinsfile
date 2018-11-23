node {
  
  stage("Pull"){
  	checkout scm
  }
  stage("build"){
  	sh 'mvn clean verify -DskipITs=true'
  	junit '**/target/surefire-reports/TEST-*.xml'
   }

}