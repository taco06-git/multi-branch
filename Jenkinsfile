pipeline {
    agent none

    stages {
        stage('Run on PRODUCTION') {
            when {
                branch 'PRODUCTION'
            }
            agent {
                label 'PROD'
            }
            steps {
                echo "Code pushed to PRODUCTION branch"
                echo "Running job on PROD agent"
                sh 'cat job'  // ✅ shell step to print the file named 'job'
            }
        }

        stage('Run on DEVELOPMENT') {
            when {
                branch 'DEVELOPMENT'
            }
            agent {
                label 'DEV'
            }
            steps {
                echo "Code pushed to DEVELOPMENT branch"
                echo "Running job on DEV agent"
                sh 'cat job'  // ✅ shell step to print the file named 'job'
            }
        }
    }
}

