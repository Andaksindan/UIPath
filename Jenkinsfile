pipeline {
  agent any
  environment {
      MAJOR = '1'
      MINOR = '0'
  }
  stages {
    stage ('Build') {
      steps {
        UiPathPack (
          outputPath: "Output\\${env.BUILD_NUMBER}",
          projectJsonPath: "C:\Users\ASUS\Documents\UiPath\UIPath\project.json",
          version: [$class: 'ManualVersionEntry', version: "${MAJOR}.${MINOR}.${env.BUILD_NUMBER}"]
          useOrchestrator: true,
          traceLoggingLevel: "Information",
          orchestratorAddress: "https://cloud.uipath.com",
          orchestratorTenant: "DefaultTenant",
          credentials: [$class: 'Piyush Gedam', credentialsId: “Vac1”]
        )
      }
    }
  }
}
