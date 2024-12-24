pipeline {
    agent any
    environment {
        //our own custom env variables
        DEPLOY_TO = 'xyzabc'
    }
    stages {
        stage('Deploy to Dev') {
            steps {
                echo "deploying to dev env"
            }
        }
        stage('ProdDeploy') {
            when {
                anyOf {
                    //10 conditions present , anyone should be satisfied
                    branch 'production'
                    environment name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps {
                echo "deploying to production"
            }
        }
    }
}
