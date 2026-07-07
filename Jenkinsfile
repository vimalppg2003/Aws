pipeline{
      parameters{
        string(name: 'SOURCE_FILE',description: 'Enter your path file',defaultvalue: 'index.html')
        string(name: 'DESTINATION FILE',description: 'enter your target path',defaultvalue: 'index.nginx-debian.html')
        choice(name:'SERVICE',choices:['nginx,apache,docker'],description: 'enter your service name')
      }
    agent any
    stages{
        stage('Build'){
            steps{
                sh """
                    echo "runing Build stage"
                    sudo cp ${params. 'SOURCE_FILE '} /var/www/html/${params.'DESTINATION FILE'}
                    echo "Build completed"
                """
            }
        }
        stage('Deploy'){
            steps{
                sh """
                    echo "runing Deploy stage"
                    sudo systemctl restart ${params.'SERVICE'}
                    echo "Deploy completed"
                """
            }
        }
    }
}
