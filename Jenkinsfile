pipeline {
    agent  any
    stages {
        stage('build') {
            steps {
                echo  'build done'
            }
        }
        stage('deployments') {
            parallel {
                stage('deploy to stg') {
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
