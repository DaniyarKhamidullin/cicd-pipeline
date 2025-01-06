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
        git(url: 'https://github.com/DaniyarKhamidullin/cicd-pipeline/scripts/build.sh', branch: 'main', credentialsId: 'DaniyarKhamidullin_id')
      }
    }

  }
  environment {
    DOCKERHUB_CREDENTIALS = 'ubiwk_id'
  }
}