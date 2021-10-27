pipeline {
  agent any
  stages {
    stage('UAT') {
      parallel {
        stage('UAT') {
          steps {
            sh 'echo "this is a build stage for UAT env"'
            input(message: 'waiting for approval', id: '1', submitter: 'admin', submitterParameter: 'approve', ok: 'approve')
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