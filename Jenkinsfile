pipeline {
    agent any
    stages {
        stage ("Build") {
            steps {
                sh 'docker build -t pavanreddy215/paytm:bus .'
            }
        }
        
        stage ("Deploy") {
            steps {
                sh 'docker run -itd --name bus -p 8888:80 pavanreddy215/paytm:bus'
            }
        }
    }
}
