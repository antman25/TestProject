library 'jenkins-shared-lib'

//withEnv(["DOCKER_CREDENTIALS=nexus_auth"]) {
//  runNodeSvcPipeline([
//    repository: ''
//  ])
//}

podTemplates.dockerTemplate {
    node(POD_LABEL) {
      stage('Checkout Code') {
        checkout scm
        config.commitHash = sh(returnStdout: true, script: 'git rev-parse HEAD').trim().take(7)
        currentBuild.displayName = "#${BUILD_ID}-${config.commitHash}"
      }
      buildDockerImage config
    }
  }
