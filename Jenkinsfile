pipeline {
    agent any

    tools {
        jdk 'JDK21'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/sphurtideshmukh-commits/MyFirstProject.git'
            }
        }

        stage('Compile Java') {
            steps {
                bat '''
                    javac src/Main.java
                '''
            }
        }

        stage('Run Program') {
            steps {
                bat '''
                    java -cp src Main
                '''
            }
        }
    }
}
