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
        sh 'cd /NSHC_WBC/NSaferWhite/NWG_exe'
        sh '''ls
chmod 755 build.sh'''
        sh './build.sh'
      }
    }

  }
}