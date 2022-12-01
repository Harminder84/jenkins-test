
   
pipeline {
    agent  any
    stages {
       stage('code building') {
           steps {
               echo 'prod deployment done'
           }
          post {
                    always {
                        jiraSendBuildInfo branch: 'test'
                    }
                }
         
       }
    }
}
