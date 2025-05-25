pipeline { 
    agent any 
 
    tools { 
        maven 'Maven-3.8.8' // Use the Maven tool configured in Jenkins 
    } 
 
    stages { 
        stage('Checkout') { 
            steps { 
                git 'https://github.com/sachinx0x/maven-project.git' 
            } 
        } 
 
        stage('Build') { 
            steps { 
                bat 'mvn clean package' 
            } 
        } 
 
        stage('Test') { 
            steps { 
                bat  'mvn test' 
            } 
        } 
 
        stage('Deploy') { 
            steps { 
                echo 'Deploying application...' 
            } 
        } 
    } 
 
    post { 
        success { 
            echo 'Build and Test Passed!' 
        } 
        failure { 
            echo 'Build Failed!' 
        } 
    } 
} 
