pipeline {
    agent any
    tools {
        nodejs 'nodejs21'
    }
    stages {
        stage('Build') {
            steps {
                echo "Ejecutar npm install" 
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
                echo "Ejecutar npm start" 
                timeout(time: 1, unit: 'MINUTES') {
                    sh 'npm start'
                }
            }
        }
    }
}
