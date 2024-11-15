pipeine block {
    agent any
    tools{maven: 'M3'}
    stages{
        stage('Checkout'){
            git branch: 'main', url: 'https://github.com/yesmine-arous/SpringPetClinic.git'
        }
        stage('Build'){
            steps{
                sh 'mvn compile'
            }
            stage('Test'){
                sh 'mvn test'
            }
            stage('Package'){
                steps{
                    sh 'mvn package'
            }
            stage('Deploy'){
                steps{
                    sh 'java -jar- /home/coder/.jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar'
            }
        }
    }
}
