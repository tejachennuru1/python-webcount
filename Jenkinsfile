pipeline {
    agent { label 'python' }
    stages {
        stage('git') {
            steps {
                branch : 'master'
                git url: 'https://github.com/tejachennuru1/python-webcount.git'
            }
        }
    }

stages {
        stage('git') {
            steps {
                branch : 'master'
                git url: 'https://github.com/tejachennuru1/python-webcount.git'
            }
        }
}

stages {
        stage('archive artifact') {
            steps {
               archiveArtifacts artifacts: '.tox/distwebcount-01.zip'

stages {
        stage('junit publish') {
            steps {
               junit "**/*.xml"

            }
        }

}
            }

        }
}