@Library('pipeline-library') _
pipeline {
  agent any
  stages {
    parallel {
      stage('Stage1') {
        steps {
          hello()
        }
      }
      
      stage('Stage2') {
        steps {
          hello()
        }
      }
    }
  }
}
