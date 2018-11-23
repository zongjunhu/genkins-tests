node {
  
  stage("Pull"){
  	checkout scm
  }
  stage("build"){
 	'mvn package'
  }
  stage("report"){
      junit '**/target/surefire-reports/TEST-*.xml'
  }

}