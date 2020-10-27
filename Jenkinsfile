pipeline {
  agent any
  stages {

    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('kubectl apply') {
      steps {
        sh 'gcloud container clusters get-credentials anthos-cluster-us-central-1 --zone us-central1-c --project searce-anthos-lab'
        sh 'kubectl apply -f stg.yaml'
      }
    }

  }
}
