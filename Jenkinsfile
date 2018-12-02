@Library('pipeline-library') _
pipeline {
  agent any
  stages {
    stage('Prepare') {
      steps {
        hello()
        
        script {
          // Below is dynamic script
          stage('Deploy: dev', true) { 
              hello()
          }
          
          stage('Test: dev', true) {
            parallel Performance: {
              hello()
              sleep 10
            }, Regression: {
              hello()
              sleep 20
            }
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
