pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               bat "rmdir  /s /q TicketBookingServiceJunitTesting"
                bat "git clone https://github.com/kishancs2020/TicketBookingServiceJunitTesting.git"
                bat "mvn clean"
            }
        }
        stage('install') {
            steps {
                bat "mvn install"
            }
        }
        stage('test') {
            steps {
                bat "mvn test"
            }
        }
        stage('package') {
            steps {
                bat "mvn package"
            }
        }
    }
}
