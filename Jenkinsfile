pipeline {
   agent any

   stages {
      stage('Verify Branch') {
         steps {
            echo "$GIT_BRANCH"
         }
      }
      stage('Docker Build') {
             steps {
                script {
                     sh "docker images -a"
                    }
             }
          }
      stage('ShellOutFromSharedLib'){
            }
            steps {
                script {
                    def dockerVersion = shellOut('docker --version')
                    echo "Docker version on agent:\n\n${dockerVersion}"

                    sh "docker info"
                 }
          }
     }
  }
}
