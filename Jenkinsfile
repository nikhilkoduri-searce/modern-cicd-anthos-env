pipeline {

  stages {

    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('kubectl apply') {
      steps {
        sh 'kubectl apply -f stg.yaml'
      }
    }

  }
}
