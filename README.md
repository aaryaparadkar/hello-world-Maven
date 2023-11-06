## DevOps Project for Beginners   

[![Image](https://github.com/yankils/Simple-DevOps-Project/blob/master/Devops_course.PNG "DevOps Project - CI/CD with Jenkins Ansible Docker Kubernetes ")](https://www.udemy.com/course/valaxy-devops/?referralCode=8147A5CF4C8C7D9E253F)

pipeline {
    agent any
    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "Maven 3.9.5"
    }
    stages {
        stage('Clone Code') {
            steps {
                git 'https://github.com/sudhakarjha0042/hello-world-Maven.git'
            }
        }
        stage('Build Code') {
            steps {
                bat "mvn clean install"
            }
        }
    }
}
