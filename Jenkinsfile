pipeline {
  agent none
  stages {
    stage('Build & Test') {
      agent {
        node {
          label 'nshc_docker_agent'
        }

      }
      steps {
        sh 'mvn -Dmaven.test.faulure.ignore clean package'
        stash(name: 'build-test-artifacts', includes: '**/target/surefire-repo')
      }
    }

  }
}