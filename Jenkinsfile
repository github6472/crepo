pipeline{
    agent any 
    stages {
         stage( 'code pull') {
            steps {
                git branch :'master' ,url:'https://github.com/github6472/crepo.git'
                echo 'git pull successesful'
            }
        }
        stage ('code build') {
            steps {
                sh 'mvn install'
            }
        }
        stage ('run') {
            steps {
                sh '"./new_script.sh" "stdin:${1} '
            }
        }
    }
}
