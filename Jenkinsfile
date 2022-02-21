pipeline {
    agent  any
    stages {
        stage('build') {
            steps {
                echo  'build done'
            }
            post {
                 always {
                     jiraSendBuildInfo()
                 }
             }
        }
        stage('deployments') {
            parallel {
                stage('install to stg') {
                    steps {
                        echo 'stg deployment done'
                    }
                }
                stage('install to prod') {
                    steps {
                        echo 'prod deployment done'
                    }
                }
            }
        }
    }
}
