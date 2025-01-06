pipeline {
  agent {
    node {
      label 'Test'
    }

  }
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/DaniyarKhamidullin/cicd-pipeline', branch: 'main', credentialsId: 'DaniyarKhamidullin_id')
      }
    }

    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        sh './scripts/test.sh'
        sh 'q'
      }
    }

  }
}