pipeline {
  agent any
  stages {
    stage('UAT') {
      parallel {
        stage('UAT') {
          steps {
            sh 'echo "this is a build stage for UAT env"'
          }
        }

        stage('Dev') {
          steps {
            sh 'echo "this is a dev build"'
          }
        }

      }
    }

    stage('Prod') {
      steps {
        sh 'echo "this is a prod build"'
      }
    }

  }
}