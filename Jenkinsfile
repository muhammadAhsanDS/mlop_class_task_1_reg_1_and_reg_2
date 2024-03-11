pipeline {
    agent any

    stages {
        stage('Testing') {
            steps {
                script {
                    def testVariable = "test"

                    // If-else condition to check the value of the variable
                    if (testVariable == "test") {
                        // Checkout from GitHub repository
                        checkout([$class: 'GitSCM', 
                                  branches: [[name: '*/master']],
                                  userRemoteConfigs: [[url: 'https://github.com/muhammadAhsanDS/mlop_class_task_1_reg_1_and_reg_2.git']]])
                    } else {
                        echo "Not checking out from GitHub repository"
                    }
                }
            }
        }
    }
}
