pipeline {
    agent any

    stages {

        stage('Ping Server') {
            steps {
                echo "Pinging web server..."
                sh "ping -c 4 192.168.1.10"   // <--- Replace with your server IP
            }
        }

        stage('HTTP Test') {
            steps {
                echo 'Testing HTTP response...'
                sh "curl -I http://192.168.1.10:8080" // <--- Replace with your service URL/port
            }
        }

    }
}
