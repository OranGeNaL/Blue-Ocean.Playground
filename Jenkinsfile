pipeline {
  agent any
  stages {
    stage('Clone Repo') {
      steps {
        git(url: 'https://github.com/OranGeNaL/DD.Backend', branch: 'main', credentialsId: '1')
      }
    }

    stage('Build Image') {
      steps {
        sh 'docker build -t orangenal/dd-back:latest .'
      }
    }

  }
}