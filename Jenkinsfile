pipeline {
    agent any 
    stages {
        stage('Static Analysis') {
            steps {
                echo 'Run the static analysis to the code' 
            }
        }
        // stage('Install'){
        //     steps{
        //         bat 'mvn clean install'
        //     }
        // }
        stage('Compile') {
            steps {
                bat 'mvn compile'
                echo 'Compile the source code' 
            }
        }
        stage('Security Check') {
            steps {
                echo 'Run the security check against the application' 
            }
        }
        stage('Run Unit Tests') {
            steps {
                echo 'Run unit tests from the source code' 
            }
        }
        stage('Run Integration Tests') {
            steps {
                echo 'Run only crucial integration tests from the source code' 
            }
        }
         stage('build'){
            steps {
                bat 'mvn -DskipTests package'
            }
        }
        stage('Publish Artifacts') {
            steps {
                echo 'Save the assemblies generated from the compilation' 
            }
        }
        stage('image'){
            steps {
                echo 'creating docker image...'
            }
        }
    }
}
