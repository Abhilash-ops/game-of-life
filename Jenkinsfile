pipeline{
    agent{label 'Master'}
    triggers{ 
        upstream(upstreamProjects: 'gol', threshold: hudson.model.Result.SUCCESS)
        }
    stages{
        stage('Source'){
            steps{
                git 'https://github.com/Abhilash-ops/game-of-life.git'                

            }
            
        }
        stage('Package'){
            steps{
                bat label: '', script: 'call mvn package'
                input 'continue to next step?'
				archiveArtifacts 'gameoflife-web/target/*.war'
            }
        }
    }
}

