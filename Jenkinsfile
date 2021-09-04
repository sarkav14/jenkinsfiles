pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn -B package'
      }
    }

    stage('Docker Push ') {
      steps {
        sh '''docker push {repositoru url}:{tag}
'''
      }
    }

    stage('Deploy in Docker Compose') {
      steps {
        sh '''ssh 
cd
docker compose up '''
      }
    }

  }
  tools {
    maven 'M3'
  }
}