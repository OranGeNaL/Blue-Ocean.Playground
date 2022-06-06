pipeline {
  agent any
  stages {
    stage('Clone Repo') {
      agent {
        node {
          label 'docker'
        }

      }
      steps {
        git(url: 'https://github.com/OranGeNaL/DD.Backend', branch: 'main', credentialsId: '1')
      }
    }

    stage('Build Image') {
      agent {
        node {
          label 'docker'
        }

      }
      steps {
        sh 'docker build -t orangenal/dd-back:latest .'
      }
    }

  }
}