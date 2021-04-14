pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'this is the kartiks build job'
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        echo 'this is the test kartik job'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'this is the 3 package job'
        sh 'npm run package'
        sleep 7
      }
    }

    stage('archieve') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}