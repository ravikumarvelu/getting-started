pipeline {
    agent {
        docker {
            image 'docker:dind'
            args '-u root:root -p 3000:3000 --privileged -v /var/run/docker.sock:/var/run/docker.sock'
        }
    }

    environment {
        CI = 'true'
    }

    stages {
        stage('docker build') {
            steps {
                sh 'docker build  -t myrepo/myapp .'
            }
        }
    }
}
