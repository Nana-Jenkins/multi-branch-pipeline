pipeline {   
    agent any
    tools {
        maven 'maven-3.9'
    }
    stages {
        stage("test") {
            steps {
                script {
                    echo "Testing the application..."
                    echo "Executing pipeline for ${BRANCH_NAME}"
                }
            }
        }

        stage("build") {
            when{
                expression{

                    BRANCH_NAME == 'master'

                }

            }
            steps {
                script {
                
                echo "Building the application"


                }
            }
        }

        stage("deploy") {

            when {

                expression{

                    BRANCH_NAME = "master"

                }
            }
            steps {
                script {
                    echo "Deploying the application...."
                }
            }
        }               
    }
}