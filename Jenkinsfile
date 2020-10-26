pipeline {
  agent none
  stages {
    stage('Build & Test') {
      agent {
        node {
          label 'WBC Test Server'
        }

      }
      steps {
        sh '''cd NSHC_WBC
ls'''
        stash(name: 'build-test-artifacts', includes: '**/target/surefire-reports/TEST=*.xml,target/*.jar')
      }
    }

    stage('Report & Publish') {
      agent {
        node {
          label 'docker'
        }

      }
      steps {
        unstash 'build-test-artifacts'
        junit '**/target/surefire-reports/TEST-*xml'
        archiveArtifacts(artifacts: 'target/*.jar', onlyIfSuccessful: true)
      }
    }

  }
}