pipeline{
    agent any
// uncomment the following lines by removing /* and */ to enable
/*    tools{
       maven 'Maven 3.6.3' 
    }
*/    
    stages{
        stage('build'){
            steps{
                echo 'Running Build Job....'
                sh 'mvn compile'
                sleep 4
            }
        }
        stage('test'){
            steps{
                echo 'Running Test Job....'
                sh 'mvn clean test'
                sleep 9
            }
        }
        stage('package'){
            steps{
                echo 'Packaging Application.....'
                sh 'mvn package -DskipTests'
                sleep 7
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
