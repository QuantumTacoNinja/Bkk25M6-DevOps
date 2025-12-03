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
                    go build -o appbin main.go
                    ./main
                """
            }
        }
    }
}
