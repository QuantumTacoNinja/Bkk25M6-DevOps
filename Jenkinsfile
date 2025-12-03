pipeline {
    agent any

    tools {
        go "1.24.1"
    }

    stages {
        stage('Build') {
            steps {
                sh """
                    go build -o main /var/lib/jenkins/workspace/myapp-build-pipeline/app/main.go
                    /var/lib/jenkins/workspace/myapp-build-pipeline/main
                """
            }
        }
    }
}
