pipeline {
    agent any
    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 60, unit: 'SECONDS')
    }
    stages {
        stage('all') {
            steps {
                echo 'this will run in all branch'
            }
        }

        stage('Food'){
            when {
                branch comparator: 'EQUALS', pattern: 'foods'
            }
            steps {
                sh '''
                echo "this is running from foods branch"
                '''
            }
        }
    }
  
}