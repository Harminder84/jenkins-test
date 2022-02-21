pipeline {
    agent  any
    stages {
        stage('build') {
            steps {
                echo  'build done'
            }
            post {
                 always {
                     jiraSendBuildInfo branch: 'TEST-123-awesome-feature'
                 }
             }
        }
        stage('deployments') {
            parallel {
                stage('deploy to stg') {
                    steps {
                        echo 'stg deployment done'
                    }
                }
                stage('install to contigency') {
                    steps {
                        echo 'prod deployment done'
                    }
                    post {
                        always {
                            jiraSendDeploymentInfo environmentId: 'us-prod-1', environmentName: 'us-prod-1', environmentType: 'Contigency'
                        }
                    }
                }
            }
        }
    }
}
