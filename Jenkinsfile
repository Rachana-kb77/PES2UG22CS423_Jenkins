pipeline {
    agent any
    stages {
        stage('Build') {
    steps {
        sh 'g++ main/hello.cpp -o main/hello_exec'
        echo 'Build Stage Successful'
    }
}

stage('Test') {
    steps {
        sh './main/non_existent_exec'  // Change path here
    }
}

        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
