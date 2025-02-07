node {
    def dockerImage = docker.image('node:16-buster-slim')

    dockerImage.inside('-p 3000:3000') {
        stage('Build') {
            sh 'npm install'
        }

        stage('Test') {
            sh './jenkins/scripts/test.sh'
        }
    }
}