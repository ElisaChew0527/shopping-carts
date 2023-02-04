pipeline {
  agent any
  stages {
    stage('build-the-app') {
      steps {
        echo 'build job'
        sh 'mvn compile'
      }
    }

    stage('test-the-app') {
      steps {
        echo 'test job'
        sh 'mvn test'
      }
    }

    stage('package-the-job') {
      steps {
        echo 'package job'
        sh 'mvn package'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/target/*.jar'
      }
    }

  }
  tools {
    maven 'maven'
  }
  post {
    always {
      echo 'this pipeline for shopping-carts has completed...'
    }

  }
}