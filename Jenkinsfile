pipeline {
    agent { label 'python' }
    stages {
        stage('git clone') {
            steps {
                git url: 'https://github.com/tejachennuru1/python-webcount.git',
                    branch : 'master'
            }
        }
    }

    stage('build') {
        steps {
            sh 'pip3 install -r requirements.txt'
            sh 'tox'
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
