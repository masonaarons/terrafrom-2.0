pipeline {
  agent any
  stages {
    stage('get') {
      steps {
        git 'https://github.com/masonaarons/terrafrom-2.0.git'
      }
    }

    stage('init') {
      steps {
        sh 'terraform init --reconfigure'
      }
    }

    stage('plan') {
      steps {
        sh 'terrafrom plan'
      }
    }

    stage('apply') {
      steps {
        sh 'terraform apply --auto-approve'
      }
    }

  }
}