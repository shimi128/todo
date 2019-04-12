pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
               sh "tar -czvf todo.tar.gz -C . ."
          archiveArtifacts artifacts: "todo.tar.gz", fingerprint: true
          script {
            currentBuild.displayName = "0.1"
          }
              
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
