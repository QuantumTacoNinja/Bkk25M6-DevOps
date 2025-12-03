pipeline {
    agent any

    tools {
       go "1.24.1"
    }

    stages {
        stage('Build') {
            steps {
                sh "cd app"
                sh "go build main.go"
                sh "./main"
            }
        }
    }
}
