pipeline {
    agent any

    stages {
        stage ('SCM') {
            steps {
                git branch: 'main', url: 'https://github.com/bhormohan/check'
            }
        }
        stage ('docker build image') {
            steps {
                sh '/usr/bin/docker build -t <username>/mywebsite .'
            }
        }
    }
}
