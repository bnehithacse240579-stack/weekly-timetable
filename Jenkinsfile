pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building Weekly Timetable'
                echo 'HTML project is ready'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Weekly Timetable'

                bat 'if exist index.html (echo HTML file found) else (exit /b 1)'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Weekly Timetable'

                archiveArtifacts artifacts: 'index.html'

                echo 'Deployment completed successfully'
            }
        }
    }
}