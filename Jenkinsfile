pipeline {
  agent none
  stages {
    stage('Build & Test') {
      agent {
        node {
          label 'WBC'
        }

      }
      steps {
        sh '''echo "Hello, Juyong Lee!"
cd NSHC_WBC
ls'''
      }
    }

  }
}