node {
  
  stage("Pull"){
  	checkout scm
  }
  stage("build"){
  	'mvn clean verify -DskipITs=true'
  	junit '**/target/surefire-reports/TEST-*.xml'
   }

}