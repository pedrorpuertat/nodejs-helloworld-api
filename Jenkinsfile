pipeline {
    agent any
    tools {
        nodejs 'nodejs21'
    }
    stages {
        stage('Build') {
            steps {
                echo "Ejecutar npm install En el Server" 
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo "Ejecutar npm test push" 
                sh 'npm test'
            }
        }
        stage('Prod') {
            steps {
                echo "Ejecutar el start del proyecto" 
                sh 'npm start'
            }
        }
    }
}
