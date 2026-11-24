pipeline {
    agent any
    stages {
        stage ("Build") {
            steps {
                sh 'docker build -t vinaikumarp/abinay:bank .'
            }
        }
        stage ("Deploy") {
            steps {
                sh 'docker run -itd --name bank2 -p 4455:80 vinaikumarp/abinay:bank'
            }
        }
    }
}
