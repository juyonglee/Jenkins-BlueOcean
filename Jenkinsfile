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
        sh '''ls
cd /NSHC_WBC/
ls'''
      }
    }

  }
}