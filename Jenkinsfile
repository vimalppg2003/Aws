pipeline{
      parameters{
        string(name: 'SOURCE FILE',DESCRIPTION: 'Enter your path file',DEFAULTVALUE: 'index.html')
        string(name: 'DESTINATION FILE',description: 'enter your target path',DEFAULTVALE: 'index.nginx-debian.html')
        choice(name:'SERVICE',choice:['nginx,apache,docker'],description: 'enter your service name')
      }
    agent any
    stages{
        stage('Build'){
            steps{
                sh """
                    echo "runing Build stage"
                    sudo cp {$ params. 'SOURCE FILE '},${params.'DESTINATION FILE'}
                    echo "Build completed"
                """
            }
        }
        stage('Deploy'){
            steps{
                sh """
                    echo "runing Deploy stage"
                    ${params.'SERVICE'}
                    echo "Deploy completed"
                """
            }
        }
    }
}
