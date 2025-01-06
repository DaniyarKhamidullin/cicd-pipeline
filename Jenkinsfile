pipeline {
  agent {
    docker {
      image 'ubuntu:latest'
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