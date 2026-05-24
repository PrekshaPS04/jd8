pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
                git branch: 'main',url : 'https://github.com/PrekshaPS04/jd8.git'
            }
        }
        stage('build Image') {
            steps {
                bat 'docker build -t home8 .'
            }
        }
        stage('Run container') {
            steps {
                bat 'docker run -d -p 80:80 --name home8c home8'
            }
        }
    }
}