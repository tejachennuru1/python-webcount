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

    stage('archive artifact') {
            steps {
                archiveArtifacts artifacts: '.tox/distwebcount-01.zip'
            }
    }

        stage('junit publish') {
            steps {
                junit '**/*.xml'
            }
        }
}
