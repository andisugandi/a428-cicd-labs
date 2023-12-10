node {
    checkout scm
    withDockerContainer(args: '-v /home/a428-cicd-labs:/usr/src/app, -p 3000:3000', image: 'node:16-buster-slim'){
        stage('Build') {
                sh 'npm install'
        }
    }
}
