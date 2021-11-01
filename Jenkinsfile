pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building a JenkinsPipeline'
          }
        }

        stage('Test') {
          steps {
            echo 'Testing an application '
          }
        }

      }
    }

    stage('error') {
      steps {
        echo 'Deploying'
      }
    }

  }
}