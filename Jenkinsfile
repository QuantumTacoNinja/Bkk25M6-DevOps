pipeline {
    agent any

    tools {
        go "1.24.1"
    }

    stages {
        stage('Build') {
            steps {
                sh """
                    cd app
                    go mod tidy
                    go build -o appbin main.go
                """
            }
        }
    }
}
