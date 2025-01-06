pipeline {
  agent {
    node {
      label 'Test'
    }

  }
  stages {
    stage('test') {
      steps {
        sh 'echo "Hello World"'
        sh 'ls -la'
        sh 'pwd'
      }
    }

  }
}