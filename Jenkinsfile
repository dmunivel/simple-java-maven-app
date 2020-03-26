pipeline {
    agent {
        docker {
            image 'fcr.fmr.com/maven:3.6-jdk-8'
            args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}