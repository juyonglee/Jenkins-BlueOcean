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
        sh 'gcc -m64 -D_LINUX *.c -I. -I../../gen_include -I../../tables -L../../lib/linux_x86_64 -lNSCrypto -lNWG -o genwbtable'
      }
    }

  }
}