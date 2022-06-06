pipeline {
  agent any
  stages {
    stage('Clone Repo') {
      steps {
        git(url: 'https://github.com/OranGeNaL/DD.Backend', branch: 'main')
      }
    }

    stage('Build Image') {
      steps {
        sh 'docker build -t orangenal/dd-back:latest .'
      }
    }

  }
}