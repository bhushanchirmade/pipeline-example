@Library('pipeline-library') _
pipeline {
  agent any
  stages {
    stage('Deploy') {
      steps {
        script {
          stage('Dont display', false) { 
              hello()
          
          }

          stage('Display', true) { 
           
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
