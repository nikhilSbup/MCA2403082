pipeline{
    agent any
    
    stages{
        stage('Build'){
            steps{
                echo "Running build steps for all branches"
                echo 'mvn clean package'
            }
        }
        stage('Test'){
            steps{
                echo "Running build steps for all branches"
                echo 'mvn test'
            }
        }
        stage('Deploy'){
            when{
                branch 'main'
            }
            steps{
                echo "Deploying only on main branches"
                echo './deploy.sh'
            }
        }
    }
}
