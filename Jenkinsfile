node {
  
  stage("Pull"){
  	checkout scm
  }
  stage("build"){
  	'mvn clean verify -DskipITs=true'
  	echo "${BUILD_NUMBER}"
   }

}