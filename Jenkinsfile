pipeline {
    agent any
    parameters 
    {
        string(name: 'NAME', defaultValue: 'honey', description: 'name of the person')
        text(name: 'PARA', defaultValue: '', description: 'enter smthing')
        choice(name: 'ENV', defaultValue: ['dev', 'test', 'prod'], description: 'env u want to deploy')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'would u like to scan')
        password(name: 'PASSWORD', defaultValue: 'SECUREPASSWD', description: 'enter a passwd')
    }
    stages {
        stage('Parameter Stage') 
        {
            steps {
                echo "welcome ${params.NAME}"
                echo "What to do ${params.PARA}"
                echo "deploying ${params.ENV}"
                echo "are scans happening: ${params.TOGGLE}"
                echo "the password is: ${params.PASSWORD}"

            }
        }
    }
}

