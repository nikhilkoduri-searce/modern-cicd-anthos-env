pipeline {
  agent any
  stages {

    stage('Checkout') {
      steps {
        checkout scm
      }
    }

  stage('Deploy kubectl') {
            steps{
                step([$class: 'KubernetesEngineBuilder',
                        projectId: "searce-anthos-lab",
                        clusterName: "nikhil-research-cluster",
                        zone: "us-central1-c",
                        manifestPattern: 'stg.yaml',
                        credentialsId: "searce-anthos-lab",
                        verifyDeployments: true])
  }
  }
  }
}
