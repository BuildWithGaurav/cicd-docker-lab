pipeline {
    agent any

    stages {
        stage('Build Image') {
            steps {
                sh 'docker build -t buildwithgaur/cicd-lab-app .'
            }
        }

        stage('Push Image') {
            steps {
                sh '''
                docker login -u buildwithgaur -p Acchaji@100
                docker push buildwithgaur/cicd-lab-app
                '''
            }
        }
    }
}
