pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    stages {
        stage('Build') {
            steps {
                dir('MyMavenApp') {
    sh 'mvn clean package'
}
            }
        }
    }

    post {
        failure {
            echo 'Build failed!'
        }
        success {
            echo 'Build successful!'
        }
    }
}
