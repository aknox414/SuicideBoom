pipeline {
  agent {
    docker {
      image 'maven:3.5.2-jdk-9'
    }
    
  }
  stages {
    stage('Say Hello') {
      steps {
        echo 'Hello World!'
        sh 'go version'
      }
    }
  }
}