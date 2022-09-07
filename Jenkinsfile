CODE_CHANGES = true
pipeline {
    agent any
    stages {
        stage('Build') {
            when {
                expression {
                    BRANCH_NAME == 'main' && CODE_CHANGES == true   
                }
            }
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            //when is this going to be run?
            when {
                expression {
                    BRANCH_NAME == 'main' || BRANCH_NAME == 'master'   
                }
            }
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    
    post { // define expressions of 
        always { //always executed, on failure, success, anything
            echo 'Always'
        }  
    }
}
