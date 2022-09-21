pipeline {
  agent none
  stages {
    stage('app test') {
      agent any
      when {
        branch 'feature-*'
      }
      steps {
        echo 'testing python App'
        dir(path: 'tests') {
          sh 'export GIT_BRANCH'
          sh 'export AUTH_TOKEN'
          sh 'export PROJECT'
          sh 'export BUNNY_URL_API'
          sh 'echo Happy birthday!'
        }

      }
    }

  }
  post {
    always {
      echo 'Pipeline finished executing'
    }

  }
}