pipeline {
    agent any
    stages {
    stage('checkout '){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/feat-project2']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/prjpracticeteam/githubpractice.git']]])
            }
        }
        stage('docker image  build') {
            steps {
                sh 'docker build .'
            }
        }
        stage(' '){
            steps{
                git branch: 'feat-project2', url: 'https://github.com/prjpracticeteam/githubpractice.git'
            }
        }
    }
}
