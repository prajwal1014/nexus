pipeline{
    agent any
    tools{
        maven 'maven'
    }
    stages{
        stage('verify'){
            steps{
                sh 'mvn clean verify'
            }
        }
        stage('build'){
            steps{
                sh 'mvn clean package'
            }
        }
        stage('deploy'){
            steps{
                sh 'mvn -s settings.xml clean deploy'
            }
        }
    }
}
