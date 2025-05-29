pipeline{
    agent any

    stages{
        stage('Clone'){
            steps{
                echo 'Cloning the Repo'
                git branch: 'main', url: 'https://github.com/Erik-rosol/Jenkins-Trainning.git'
            }
        }
        stage('Build'){
            steps{
                echo 'Building the project...'
                sh 'mvn clean package -DskipTests=true'
            }
        }
        stage('Test'){
            steps{
                echo 'Run the tests'
                sh 'mvn test -e'
            }
        }
    }
}