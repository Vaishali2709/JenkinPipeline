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

        stage('Test Log') {
          steps {
            writeFile(file: 'Logtextfile.txt', text: 'This is an automated file ')
          }
        }

      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            echo 'Deploying'
            input(message: '"Do you want to deploy"', id: 'OK')
          }
        }

        stage('Archive') {
          steps {
            archiveArtifacts 'Logtextfile.txt'
          }
        }

      }
    }

  }
  environment {
    chromeDriver = 'C:\\Users\\vaising2\\Downloads\\chromedriver_win32\\chromedriver.exe'
  }
}