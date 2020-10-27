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
        sh '''cd /NSHC_WBC/NSaferWhite


./wbc.sh'''
      }
    }

  }
}