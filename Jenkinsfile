pipeline {
  agent any
  stages {
    stage('Build Image') {
      agent {
        node {
          label 'docker'
        }

      }
      steps {
        git(url: 'https://github.com/OranGeNaL/DD.Backend', branch: 'main', credentialsId: '1')
        sh 'docker build -t orangenal/dd-back:latest .'
      }
    }

  }
}