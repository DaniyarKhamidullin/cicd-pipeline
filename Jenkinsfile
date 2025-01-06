pipeline {
  agent {
    docker {
      image 'node:7.8.0'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Bulid') {
      steps {
        git(url: 'scripts/build.sh', branch: 'origin', credentialsId: 'DaniyarKhamidullin_id')
      }
    }

    stage('Test') {
      steps {
        git(url: 'scripts/test.sh', branch: 'origin', credentialsId: 'DaniyarKhamidullin_id')
      }
    }

  }
  environment {
    DOCKERHUB_CREDENTIALS = 'ubiwk_id'
  }
}