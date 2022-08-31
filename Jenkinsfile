pipeline {
  agent any
  stages {
    stage('build-app') {
      steps {
        echo 'this is the build job'
        sh 'npm install'
        sleep 4
      }
    }

    stage('test-app') {
      steps {
        echo 'this is the test job'
        sh 'npm test'
        sleep 9
      }
    }

    stage('package-app') {
      steps {
        echo 'this is the package job'
        sh 'npm run package'
        sleep 7
      }
    }

    stage('archive-app') {
      steps {
        archiveArtifacts '**/Distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'Hey this my first pipeline code..'
    }

  }
}