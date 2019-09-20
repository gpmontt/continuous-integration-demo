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
        stage('build') {
          steps {
            sh '''pwd
mkdir build
cd build
cmake ..
make 
'''
          }
        }
      }
    }
  }
}