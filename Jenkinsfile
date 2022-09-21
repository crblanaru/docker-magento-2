pipeline {
   agent none

   stages {

        stage('app test') {
            when {
                branch 'feature-*'
                //     changeset '**/app/**'
            }
            agent any

            steps {
                echo 'testing python App'
                dir('app/tests'){ #create directory relatvie to root
                    // The AUTH_TOKEN and PROJECT should be set from your Jenkins setup
                    sh 'export GIT_BRANCH'
                    sh 'export AUTH_TOKEN'
                    sh 'export PROJECT'
                    sh 'export BUNNY_URL_API'
                    sh 'echo Happy birthday!'
                    // sh 'bash ./bunnycli.sh' #diff command in sh 
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