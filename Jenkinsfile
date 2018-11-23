node {
  
  
  stage("Pull"){
  	checkout scm
  }
  stage("build"){
	def mvnHome = tool 'M3'
  	sh '${mvnHome}/bin/mvn clean verify -DskipITs=true'
  	echo "${BUILD_NUMBER}"
  	sh 'ls -l'
   }

}