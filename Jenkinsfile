pipeline{
    agent any
    tools{maven 'M3'}
    stages{
            stage('Checkout'){
                steps{
                    git branch: 'main',
                    url: 'https://github.com/shashidhar2301/SpringPetClinic.git'
                }
            }
            stage('Build'){
                steps{
                    sh 'mvn compile'
                }
            }
            stage('Test'){
                steps{
                    sh 'mvn test'
                }
            }
            stage('Package'){
                steps{
                    sh 'mvn package'
                }
            }
            stage('Deploy'){
                steps{
                    sh 'java -jar /home/coder/.jenkins/workspace/PetClinicDeclarative/target/*.jar'
                }
            }
        }
}
