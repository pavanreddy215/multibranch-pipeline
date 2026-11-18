pipeline {
    agent any
    stages {
        stage ("Build") {
            steps {
                sh 'docker build -t pavanreddy215/paytm:train .'
            }
        }
        stage ("Deploy") {
            steps {
                sh 'docker run -itd --name train -p 9999:80 pavanreddy215/paytm:train'
            }
        }
    }
}
