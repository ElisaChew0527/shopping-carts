pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       maven 'maven' 
    }
    

    stages{
        stage('build-the-app'){
            steps{
                echo 'build job'
                sh 'mvn compile'               
            }
        }
        stage('test-the-app'){
            steps{
                echo 'test job'
                sh 'mvn test'                
            }
        }
        stage('package-the-job'){
            steps{
                echo 'package job'
                sh 'mvn package'                
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline for shopping-carts has completed...'
        }
        
    }
    
}
