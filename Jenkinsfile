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
}
}
