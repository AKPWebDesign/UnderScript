pipeline {
  agent {
    docker { image 'node:8-alpine' }
  }
  stages {
    stage('Setup') {
      steps {
        sh 'node --version'
        sh 'npm --version'
        sh 'npm install -g gulp-cli'
      }
    }
    stage('Build') {
      steps {
        sh 'npm run build'
      }
    }
    stage('Deploy') {
      steps {
        sh 'ls -la'
        sh 'no deploy yet lol'
      }
    }
  }
}
