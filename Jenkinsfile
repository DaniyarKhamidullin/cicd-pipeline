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
      }
    }

    stage('Docker image built') {
      steps {
        sh 'docker build -t ubiwk/epamcicd .'
      }
    }

    stage('Docker login') {
      steps {
        sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login --username $DOCKERHUB_CREDENTIALS_USR --password-stdin'
      }
    }

    stage('Docker push image') {
      steps {
        sh 'docker push ubiwk/epamcicd'
      }
    }

  }
}