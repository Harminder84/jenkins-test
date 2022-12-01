
   
pipeline {
    agent  any
    stages {
       stage('deploy to prod') {
           steps {
               echo 'prod deployment done'
           }
          post {
                 always {
                     jiraSendBuildInfo branch: 'TEST-123-awesome-feature'
                 }
             }
       }
    }
}
