pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args 'args \'-v /root/.m2:/home/jenkins/.m2\''
    }
    
  }
  stages {
    stage('Initialize') {
      steps {
        sh '''echo ${PATH}
mvn clean'''
      }
    }
  }
}