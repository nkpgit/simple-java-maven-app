pipeline {
  agent any
  stages {
    stage('SonarScan') {
      parallel {
        stage('SonarScan') {
          steps {
            echo 'Sonar Scan Start'
          }
        }

        stage('Sonar Report') {
          steps {
            echo 'Sonar Report'
          }
        }

      }
    }

    stage('Unit Test') {
      steps {
        echo 'Unit test started'
      }
    }

    stage('Code Build') {
      steps {
        echo 'Build'
      }
    }

    stage('Test') {
      steps {
        echo 'Test'
      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            echo 'Deploy'
          }
        }

        stage('Mail Send') {
          steps {
            emailext(subject: 'Deploy Completed', body: 'Deploy done', from: 'noreply@mycomny.com', to: 'developer@mycompany.com')
          }
        }

      }
    }

  }
}