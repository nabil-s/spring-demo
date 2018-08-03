node {
    docker.iamge('maven:3-alpine').inside('-v $HOME/.m2:/root/.m2') {
        stage('Build') {
            echo 'Building...'
        }
        stage('Scan') {
            echo 'Scanning...'
            sh 'mvn -DskipTests clean install sonar:sonar'
        }
        stage('Test') {
            echo 'Testing...'
        }
        stage('Deploy') {
            echo 'Deploying...'
        }
    }
}