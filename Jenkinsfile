pipeline{
    agent any
    tools{maven 'M3'}
    stages{
        stage('gitcheckout'){
            steps{
                git branch: 'main',
                url: 'https://github.com/im-kunal/SpringPetClinic.git'
            }
        }
        stage('compile'){
            steps{
                sh 'echo Hello World'
                sh 'mvn compile'
            }
        }
        stage('test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('deploy'){
            steps{
                sh 'java -jar /var/lib/jenkins/workspace/petclinic-pipeline/target/*.jar'
            }
        }
    }
}
