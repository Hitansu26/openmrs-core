pipeline{
    agent{
        label "MAVEN"
    }
    options {
        timeout(time: 30, unit: 'MINUTES')
    }
    
    stages{
        stage("GIT"){
            steps{
                git url: 'https://github.com/Hitansu26/openmrs-core.git',
                    branch: 'dev'
            }
        stage("BUILD"){
            steps{
                sh 'mvn clean package'
            }
        }
          
        }
    }

}