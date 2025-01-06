pipeline {
  agent {
    node {
      label 'Test'
    }

  }
  stages {
    stage('Bulid') {
      steps {
        git(url: 'scripts/build.sh', branch: 'main', credentialsId: 'DaniyarKhamidullin_id')
      }
    }

    stage('Test') {
      steps {
        git(url: 'scripts/test.sh', branch: 'main', credentialsId: 'DaniyarKhamidullin_id')
      }
    }

  }
  environment {
    DOCKERHUB_CREDENTIALS = 'ubiwk_id'
  }
}