pipeline {
  agent {
    kubernetes {
      label 'node'
      containerTemplate {
        name 'node'
        image 'node:8-alpine'
        ttyEnabled true
        command 'cat'
      }
    }
  }
  stages {
    stage('Setup') {
      steps {
        sh 'node --version'
        sh 'npm --version'
        sh 'npm install -g gulp-cli'
        sh 'npm install'
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
