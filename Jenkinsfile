pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo "$GIT_BRANCH"
                sh 'docker images -a'
            }
        }


    stage('test') {
        steps {
            sh 'mvn test'
        }
        post {
            always {
            junit(
                allowEmptyResults: true,
                testResults: '*/test-reports/.xml'
                )
            }
        }
    }

    // stage('build package') {
    //     steps {
    //         sh 'mvn clean package'
    //     }
    // }
    // stage('build image') {
    //     steps {
    //     // One or more steps need to be included within the steps block.
    //     }
    }
}