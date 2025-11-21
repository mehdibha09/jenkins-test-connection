pipeline {
    agent any

    stages {

        stage('Ping Server') {
            steps {
                echo "Pinging web server..."
                sh "ping -c 4 10.0.4.5"   // <--- Replace with your server IP
            }
        }

        stage('HTTP Test') {
            steps {
                echo 'Testing HTTP response...'
                sh "curl -I http://10.0.4.5:8080" // <--- Replace with your service URL/port
            }
        }

    }
}
