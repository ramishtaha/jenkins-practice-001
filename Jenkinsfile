pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'sudo docker rm static'
                sh 'sudo docker run --name static -d -p 80:80 nginx'
                sh 'sudo docker cp index.html static:/usr/share/nginx/html/index.html'
            }
        }
        stage('Test') {
            steps {
                sh 'STATUS=$(curl -s -o /dev/null -w \"%{http_code}\" http://www.example.org/)'
                sh 'echo $STATUS'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Work in Progress'
            }
        }
    }
}