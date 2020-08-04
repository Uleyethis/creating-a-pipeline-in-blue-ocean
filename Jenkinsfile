pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Initialization') {
      environment {
        PATH = '${dockerHome}/bin:${env.PATH}'
      }
      steps {
        tool(name: 'dockerHome', type: 'myDocker')
      }
    }

    stage('Build') {
      agent {
        docker {
          image 'node:6-apline'
          args '-p 3000-3000'
        }

      }
      steps {
        sh 'npm install'
      }
    }

  }
  environment {
    PATH = '${dockerHome}/bin:${env.PATH}'
  }
}