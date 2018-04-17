library 'SharedLibs'
pipeline {
  agent any
  stages {
    stage('Say Hello') {
      steps {
        echo "Hello ${My_NAME}!"
      }
    }
     stage('Shared Lib') {
         steps {
             helloWorld("Jenkins")
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
