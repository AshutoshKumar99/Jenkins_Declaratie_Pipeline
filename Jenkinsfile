pipeline {
    agent {
        label 'flower'
    }
    stages {
        stage('Checkout code from github') {
            steps 
            {
             
			checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '6ac55625-e447-4b45-a87b-c73fc21a925c', url: 'https://github.com/AshutoshKumar99/Jenkins_Declaratie_Pipeline.git']]])

            }
        }
		
		stage('Code build')
		{
		steps
		{
		bat 'mvn clean install'
		
		}
		
		}
		
		
    }
}