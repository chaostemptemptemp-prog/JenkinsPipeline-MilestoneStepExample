pipeline {
    agent any
    stages {
        stage ('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/<student-username>/<repo-name>.git'
            }
        }
        stage ('Build') {
            steps {
                bat 'python -m py_compile app.py'
                sleep(time: 15, unit: 'SECONDS')
                milestone (1)
                echo 'Build stage passed milestone 1'
            }
}
        stage ('Deploy') {
            steps {
                milestone (2)
                echo 'Deploying application....'
            }
        }
    }
}