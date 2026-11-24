pipeline {
    agent any
    stages {
        stage ("Build") {
            steps {
                sh 'docker build -t vinaikumarp/abinay:bus .'
            }
        }
        
        stage ("Deploy") {
            steps {
                sh 'docker run -itd --name bus -p 8888:80 vinaikumarp/abinay:bus'
            }
        }
    }
}
