pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker stop static'
                sh 'docker rm -f static'
                sh 'docker run --name static -d -p 80:80 nginx'
                sh 'docker cp index.html static:/usr/share/nginx/html/index.html'
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
                sh 'echo "Deploying"'
            }
        }
    }
}