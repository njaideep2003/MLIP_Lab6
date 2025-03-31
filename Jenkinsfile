pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat '''
                echo In C or Java, we can compile our program in this step
                echo In Python, we can build our package here or skip this step
                '''
            }
        }

        stage('Test') {
            steps {
                bat '''
                echo Test Step: We run testing tool like pytest here

                :: Initialize Conda (usually already available if installed properly)
                call "%USERPROFILE%\\miniconda3\\Scripts\\activate.bat"

                :: Activate environment
                call conda activate mlip

                :: Run pytest
                pytest
                '''
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                echo In this step, we deploy our project
                echo Depending on the context, we may publish the project artifact or upload pickle files
                '''
            }
        }
    }
}
