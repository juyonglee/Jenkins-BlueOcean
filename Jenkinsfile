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
        sh 'ls'
        sh 'mvn -Dmaven.test.failure.ignore clean package'
        stash(name: 'build-test-artifacts', includes: '**/target/surefire-reports/TEST-*.xml,target/*.jar')
      }
    }

  }
}