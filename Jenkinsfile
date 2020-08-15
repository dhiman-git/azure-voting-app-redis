pipeline {
   agent any

   stages {
      stage('Verify Branch') {
         steps {
            echo "$GIT_BRANCH"
         }
      }
      stage('ShellOutFromSharedLib'){
            agent {
                label 'docker-dood'
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
