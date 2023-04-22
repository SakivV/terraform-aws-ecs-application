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
                sh 'terraform init -reconfigure'
            }
        }
        stage('ValidateTerraformCode') {
            steps {
                sh 'terraform validate'
            }
        }
        stage('TerraformPlan') {
            steps {
                sh 'terraform plan -out ecs_plan.tfplan'
            }
        }
         stage('TerraformApply') {
            steps {
                sh 'terraform apply ecs_plan.tfplan'
            }
        }
    }
}
