pipeline {
agent any
stages {
stage ("SCM"){
steps {git 'https://github.com/awspandian/sam-0803.git'}
}
stage ("Build"){
steps {
		sh 'mvn clean'
		sh 'mvn install' }
}
stage ("Docker Image build") {
  when {
     branch 'master'
       }
steps {
	script {
	  app = docker.build("dockerpandian/0609")
          app.inside {
              sh 'echo $(curl localhost:8080)'
}
}
}
}
}
