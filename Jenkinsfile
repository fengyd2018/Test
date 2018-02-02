pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v /root/.m2:/home/jenkins/.m2'
    }
    
  }
  stages {
    stage('Initialize') {
      steps {
        sh 'mvn --version'
      }
    }
    stage('Firefox') {
      parallel {
        stage('Firefox') {
          steps {
            echo 'FireFox'
          }
        }
        stage('Chrome') {
          steps {
            echo 'Chrome'
          }
        }
      }
    }
    stage('Test') {
      steps {
        echo 'Test'
      }
    }
  }
}