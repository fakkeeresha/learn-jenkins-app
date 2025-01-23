pipeline {
    agent any

    stages {
        stage('w/o docker') {
            steps {
                sh 'echo "Hello............"'
            }
        }
        stage('Test'){
            steps{
                sh '''
                test -f build/index.html
                '''
            }
        }
    }
}
