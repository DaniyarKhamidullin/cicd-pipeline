pipeline {
  agent {
    node {
      label 'test'
    }

  }
  stages {
    stage('Bulid') {
      steps {
        git(url: 'https://github.com/DaniyarKhamidullin/cicd-pipeline/blob/main/scripts/build.sh', branch: 'main', credentialsId: 'DaniyarKhamidullin_id')
      }
    }

    stage('Test') {
      steps {
        git(url: 'https://github.com/DaniyarKhamidullin/cicd-pipeline/blob/main/scripts/test.sh', branch: 'main', credentialsId: 'DaniyarKhamidullin_id')
      }
    }

  }
  environment {
    DOCKERHUB_CREDENTIALS = 'ubiwk_id'
  }
}