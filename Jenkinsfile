pipeline {
    agent any
    triggers { pollSCM('* * * * *') }
    stages {
        stage('Checkout') {
            steps {
                echo "$GIT_BRANCH"
                sh 'docker images -a'
            }
        }

    // stage('build') {
    //     steps {
    //         mvn 
    //     }
    // }

    // stage('test') {
    //     steps {
    //     // One or more steps need to be included within the steps block.
    //     }
    // }

    // stage('build image') {
    //     steps {
    //     // One or more steps need to be included within the steps block.
    //     }
    }
}