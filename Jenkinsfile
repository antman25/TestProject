library 'jenkins-shared-lib'

myTest()

withEnv(["BRANCH_NAME=main"]) {
  runNodeSvcPipeline([
    repository: ''
  ])
}

