pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -c main/new.cpp' 
                sh 'g++ -o new main/new.cpp'
                sh 'Build successful'
            }
        }
        stage('Test') {
            steps {
                sh './new' 
                echo 'test stage executed successfully'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment successful'
                }
            }
}
  post{
    failure {
      echo 'Pipeline failure'
    }
  }
}
