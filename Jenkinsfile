@Library('pipeline-library') _
pipeline {
  agent any
  stages {
    stage('Deploy') {
      steps {
        script {
          stage('Dont display', false) { 
            steps {
              hello()
            }
          }

          stage('Display', true) { 
            steps {
              hello()
            }
          }
        }
      }
    }
  }
}

def stage(name, execute, block) {
    return stage(name, execute ? block : { echo "Hello" })
}
