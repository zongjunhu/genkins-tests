node {
  
  tools {
      maven "M3"
  }

  stage("Pull"){
  	checkout scm
  }
  stage("build"){
  	sh 'mvn package'
  }
}