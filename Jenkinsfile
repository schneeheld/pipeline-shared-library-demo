@Library('pipeline-library-demo')_

pipeline {
    agent none
    stages {
        stage('Demo') {
            agent any
            steps {
                printHeader 'Chapter I'
                
                echo 'Hello from the master branch.'
            }
        }
        stage("Checkpoint") {
          agent none
          steps {
            checkpoint 'Completed checkpoint'
          }
        }
        stage('Progress') {
            agent any
            steps {
                printHeader 'Chapter II'
                
                echo 'Work in progress....'
            }
        }
    }
}
