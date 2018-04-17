pipeline {
  agent any
  stages {
    stage('Say Hello') {
      steps {
        echo "Hello ${params.Name}!"
      }
    }
    stage('Deploy') {
      options {
        timeout(time: 1, unit: 'SECONDS')
      }
      input {
        message 'Which Version?'
        id 'Deploy'
        parameters {
          choice(name: 'APP_VERSION', choices: '''v1.1
v1.2
v1.3''', description: 'What to deploy?')
        }
      }
      steps {
        echo 'Continuing with deployment'
      }
    }
  }
  environment {
    My_NAME = 'MARY'
  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}