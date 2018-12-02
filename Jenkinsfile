@Library('pipeline-library') _
pipeline {
  agent any
  stages {
    stage('Deploy') {
      steps {
        hello()
      }
    }
    
    stage('Tests') {
      parallel {
        stage('Performance') {
          steps {
            hello()
          }
        }

        stage('Regression') {
          steps {
            hello()
          }
        }
      }
    }
  }
}
