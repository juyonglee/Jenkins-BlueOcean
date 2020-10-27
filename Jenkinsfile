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
        sh '''cd /NSHC_WBC/NSaferWhite/NWG_exe

ls

./build.sh'''
      }
    }

  }
}