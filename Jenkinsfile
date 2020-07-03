    node('Master'){
        stage('scm'){
            git 'https://github.com/Abhilash-ops/game-of-life.git'
        }
        stage('build'){
            bat label: '', script: 'call mvn clean package'
        }
        
    }
