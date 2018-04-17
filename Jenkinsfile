pipeline {
  agent any
  stages {
    stage('Say Hello') {
      steps {
        echo "Hello ${params.Name}!"
      }
    }
  }
  environment {
    My_NAME = 'MARY'
    TEST_USER = credentials('test-user')
  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}