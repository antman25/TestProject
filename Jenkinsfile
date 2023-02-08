library 'jenkins-shared-lib'

myTest()

withEnv(["GIT_BRANCH=main"]) {
  runNodeSvcPipeline([
    repository: ''
  ])
}

