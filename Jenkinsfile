pipeline {
    agent any

    tools {
        jdk 'JDK21'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/sphurtideshmukh-commits/MyFirstProject.git'
            }
        }

        stage('Compile Java') {
            steps {
                sh '''
                    javac src/Main.java
                '''
            }
        }

        stage('Run Program') {
            steps {
                sh '''
                    java -cp src Main
                '''
            }
        }
    }
}