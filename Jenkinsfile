pipeline {
    agent any

    tools {
        go "1.24.1"
    }

    stages {
        stage('Test') {
            steps {
                sh """
                    cd app
                    go test ./...
                """
            }
        }

        stage('Build') {
            steps {
                sh """
                    cd app
                    go build -o ../main main.go
                """
            }
        }

//        stage('Run') {
//            steps {
//                sh """
//                    ./main
//                """
//            }
//        }
    }
}
