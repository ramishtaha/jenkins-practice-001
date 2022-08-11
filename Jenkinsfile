pipeline {
<<<<<<< HEAD
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker rm static'
                sh 'docker run --name static -d -p 80:80 nginx'
                sh 'docker cp index.htmp static:/usr/share/nginx/html/index.html'
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
=======
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'first step'
      }
>>>>>>> 5fc2eae0e3867b39ecf2c48a271dd8cf3c3b01f6
    }

    stage('Test') {
      steps {
        echo 'second step'
      }
    }

    stage('Deploy') {
      steps {
        echo 'third step'
      }
    }

  }
}