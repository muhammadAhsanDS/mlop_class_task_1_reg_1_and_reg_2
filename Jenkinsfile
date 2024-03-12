pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/muhammadAhsanDS/mlop_class_task_1_reg_1_and_reg_2.git'
            }
        }

        stage('Set up Python') {
            steps {
                bat 'curl -o python-installer.exe https://www.python.org/ftp/python/3.9.5/python-3.9.5-amd64.exe'
                bat 'python-installer.exe /quiet InstallAllUsers=1 PrependPath=1'
                bat 'del python-installer.exe'
            }
        }
       
        stage('Install dependencies') {
            steps {
                bat 'pip install -r requirements.txt'
                bat 'pip install pytest'
            }
        }
       
        stage('Run tests') {
            steps {
                bat 'test.py'
            }
        }
    }
}
