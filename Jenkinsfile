pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'g++ -o output 1.cpp'
                build job: 'PES1UG20CS686-1'
            }
        }
        stage('Test') { 
            steps {
                sh 'cat 1.cpp'
            }
        }
        stage('Deploy') { 
            steps {
//                 sh './output'
                error 'Pipeline Failed' 
            }
        }
    }
    post{
        success{
            echo 'Pipeline Success'
        }
    	failure{
    		echo 'Pipeline Failed'
    	}
    }
}
