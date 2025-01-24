pipeline {
    agent any

    stages {
        stage('w/o docker') {
            steps {
                sh 'echo "Hello............"'
            }
        }
        stage('Test'){
            agent{
                docker{
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps{
                sh 'ls -la src'
                sh 'test -f src/App.css'
            }
        }
    }
}
