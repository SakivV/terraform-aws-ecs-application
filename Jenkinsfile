pipeline {
    agent any
    stages {
        stage('VerifyBranch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage('TerraformInit') {
            steps {
                sh 'terraform init'
            }
        }
        stage('ValidateTerraformCode') {
            steps {
                sh 'terraform validate'
            }
        }
    }
}
