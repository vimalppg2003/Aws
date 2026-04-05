pipeline{
    agent any
    stages{
        stage('Build'){
            stpes{
                sh """
                    echo "runing build stage"
                    sudo cp index.html /var/www/html/index.nginx-debian.html
                    echo "build completed"
                """
            }
        }
        stage('Deploy'){
            stpes{
                sh """
                    echo "runing deploy stage"
                    sudo systemctl restart nginx
                    echo "Deploy completed"
                """
            }
        }
    }
}
