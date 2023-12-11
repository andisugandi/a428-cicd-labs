node {
  properties(
    [
      pipelineTriggers(
        [pollSCM('H/2 * * * *')]
      )
    ]
  )
  checkout scm
  docker.image('node:16-buster-slim').withRun('-p 3000:3000'){
    withEnv(["CI=true"]){
      stage('Build') {
	sh 'npm install'
      }
    }
  }
}
