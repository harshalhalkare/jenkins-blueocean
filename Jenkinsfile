pipeline {
  agent any
  stages {
    stage('UAT') {
      parallel {
        stage('UAT') {
          steps {
            input(message: 'waiting for approval', id: '1', submitter: 'admin', submitterParameter: 'approve', ok: 'approve')
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