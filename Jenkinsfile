pipeline {
    agent any

    stages {

        stage('Instalar dependências') {
            steps {
                bat 'npm install'
            }
        }

        stage('Build') {
            steps {
                bat 'npm run build'
            }
        }

        stage('Teste') {
            steps {
                bat 'npm test'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executado com sucesso!'
        }

        failure {
            echo 'Pipeline falhou!'
        }
    }
}