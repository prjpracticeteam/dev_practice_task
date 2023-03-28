pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/task_docker']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/prjpracticeteam/dev_practice_task.git']]])
            }
        }
        stage('docker image build '){
            steps{
               sh 'docker build -t my-python .' 
            }
        }
        stage('git '){
            steps{
                git branch: 'task_docker', url: 'https://github.com/prjpracticeteam/dev_practice_task.git'
            }
        }
    }
}
