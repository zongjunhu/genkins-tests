node {
  
  stage("Pull"){
  	checkout scm
  }
  stage("build"){
 	'mvn package'
 	junit '**/target/surefire-reports/TEST-*.xml'
  }

}