pipeline {
  agent any
  stages {
    stage('go') {
      parallel {
        stage('go') {
          steps {
            sh '''pwd
echo \'test\''''
          }
        }
        stage('Init Git submodules') {
          steps {
            sh '''# Init Git submodules
git submodule init
git submodule update'''
          }
        }
      }
    }
    stage('run-clang-tidy') {
      steps {
        sh 'echo test'
      }
    }
  }
}