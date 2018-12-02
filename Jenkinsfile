@Library('pipeline-library') _
pipeline {
  agent any
  stages {
    stage('Initialize Deployment') {
      steps {
        script {
          stage('Deploy: dev', true) { 
              hello()
          }
          
          stage('Test: dev', true) { 
              hello()
          }

          stage('Deploy: trial', true) { 
              hello()
          }
          
          stage('Test: trial', true) { 
              hello()
          }
          
          stage('Deploy: prod', false) { 
              hello()
          }
          
          stage('Test: prod', false) { 
              hello()
          }

        }
      }
    }
  }
}

def stage(name, execute, block) {
  if(execute) {
    return stage(name, block)
  } else {
    return
  }
}
