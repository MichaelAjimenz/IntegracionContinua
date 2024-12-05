pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                echo "Realizando Build...."
            }
        }
        stage("Test") {
            steps {
                echo "Realizando Test...."
            }
        }
        stage("Deploy") {
            steps {
                echo "Desplegando......"
            }
        }
    }
    post {
        success {
            echo "Pipeline ejecutado exitosamente."
        }
        failure {
            echo "Pipeline falló."
        }
    }
}
