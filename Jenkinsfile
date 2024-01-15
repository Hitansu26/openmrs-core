pipeline{
    agent{
        label "MAVEN"
    }
    options {
        timeout(time: 30, unit: 'MINUTES')
    }
    triggers {
        pollSCM('* * * * *')
    } 
    stages{
        stage('urls') {
            steps{
                git url: 'https://github.com/Hitansu26/openmrs-core.git',
                    branch: 'dev'
            }
        stage('build') {
            steps{
                sh 'mvn clean package'
            }
        }
          
        }
    }

}