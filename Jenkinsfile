pipeline {
    agent any

    tools {
        go "1.24.1"
    }

    stages {
        stage('Test') {
              steps {
		sh """
		    root_path=$(pwd)
		    go test "$root_path/app/"
		"""
              }
          }

        stage('Build') {
            steps {
                sh """
		    root_path=$(pwd)
                    go build -o main "$root_path/app/main.go"
		    "$root_path/app/main"
                """
            }
        }
    }
}
