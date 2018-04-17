pipeline {
  agent any
  stages {
    stage('Say Hello') {
      steps {
        echo "Hello ${My_NAME}!"
      }
    }
  }
  environment {
    My_NAME = 'MARY'
  }
  post {
    aborted {
      echo 'Why didn\'t you push my button?'
      
    }
    
  }
}