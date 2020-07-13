pipeline{
    agent{label 'Master'}
    triggers{ pollSCM('* * * * *')}
    stages{
        stage('Clone and Compile'){
            steps{
                git branch: 'declarative',
                url: 'https://github.com/Abhilash-ops/game-of-life.git'
                bat label: '', script: 'call mvn package'

            }
            
        }
    }
}

