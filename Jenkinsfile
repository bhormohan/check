pipeline {
    agent any

    stages {
        stage ('SCM') {
            steps {
                git branch: 'main', url: 'https://github.com/bhormohan/check'
            }
        }
     stage ('docker login') {
            steps {
                sh 'echo dckr_pat_r2ytb4za-q_TLXBdsemOP_LDdKY | /usr/bin/docker login -u mohan16032001 --password-stdin'
            }
        }
      stage ('docker del image') {
            steps {
                sh '/usr/bin/docker rm --force mywebsite '
            }
        }
        stage ('docker build image') {
            steps {
                sh '/usr/bin/docker build -t mywebsite .'
            }
        }
    }
}
