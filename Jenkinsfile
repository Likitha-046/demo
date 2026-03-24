pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Likitha-046/demo.git'
            }
        }

        stage('Docker Build') {
            steps {
                // This 'steps' MUST be inside a 'stage'
                sh 'docker build -t my-flask-app .'
            }
        }

        stage('Run Script') {
            steps {
                sh 'chmod +x script.sh'
                sh './script.sh'
            }
        }
    }
}
