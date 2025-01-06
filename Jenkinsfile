pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'ubuntu:latest'
    }

  }
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/DaniyarKhamidullin/cicd-pipeline/scripts/build.sh', branch: 'main', credentialsId: 'DaniyarKhamidullin_id')
      }
    }

    stage('') {
      steps {
        sh '''pwd
whoami
ls -la'''
      }
    }

  }
  environment {
    DOCKERHUB_CREDENTIALS = 'ubiwk_id'
  }
}