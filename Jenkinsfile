pipeline {
    agent any

    stages {
        stage('git clone') {
            steps {
                git url: 'https://github.com/sandippatil17/xyz.git', branch: 'main'
            }
        }
        
        
        stage('Docker Build image') {
            steps {
                sh 'docker build -t myapp .'
            }
        }
        
        stage('Docker Run Container') {
            steps {
                sh 'docker run -d --name myappcontainer -p 80:80 myapp'
            }
        }
    }
}
