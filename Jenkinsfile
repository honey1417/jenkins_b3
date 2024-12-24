pipeline {
    agent any
    environment {
        //our own custom env variables
        DEPLOY_TO = 'production'
    }
    stages {
        stage('Deploy to Dev') {
            steps {
                echo "deploying to dev env"
            }
        }
        stage('ProdDeploy') {
            when {
                allOf {
                    branch 'qrrelease'
                    environment name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps {
                echo "deploying to production"
            }
        }
    }
}
