pipeline {
    agent any
    
tools {
    maven 'Maven'
}

    environment {
    VERSION = '1.0.0'
}

    stages {
        stage('Build') {
            steps {
                 bat 'mvn -version'
                echo "Building Version: ${VERSION}"
                echo 'Building..'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing..'
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
