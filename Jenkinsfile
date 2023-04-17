pipeline {
    agent any
    stages {
        stage('VerifyBranch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage('VerifyTerraformVersion') {
            steps {
                sh 'terraform --version'
            }
        }
    }
}
