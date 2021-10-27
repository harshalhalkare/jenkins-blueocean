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
        input(message: 'waiting for approval', id: 'approval id', ok: 'approve', submitter: 'harshal', submitterParameter: 'approve')
        sh 'echo "this is a prod build and i will execute once got approval from harshal"'
      }
    }

  }
}