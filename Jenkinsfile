pipeline {
    agent any


    environment {
    VERSION = '1.0.0'
}
parameters {
    booleanParam(name: 'executeTests', defaultValue: true, description: 'Run Test Stage?')
}

    stages {
        stage('Build') {
            steps {
                echo "Building Version: ${VERSION}"
                echo 'Building..'
            }
        }
stage('Test') {
    when {
        expression { params.executeTests == true }
    }
    steps {
        echo 'Running Tests...'
    }
}


        stage('Deploy') {
            steps {
                echo 'Deploying..'
            }
        }
    }

post {
    always {
        echo 'Pipeline Completed Successfully!'
    }
}
}
