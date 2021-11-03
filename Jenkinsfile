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
            echo "Get the driver Path ${chromeDriver}"
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
  environment {
    chromeDriver = 'C:\\Users\\vaising2\\Downloads\\chromedriver_win32\\chromedriver.exe'
  }
}