pipeline{
    agent any
    stages{
        stage("Checkout the code"){
            steps{
                git branch:"master", url:"https://github.com/hardikupadhyay-dg/ci-cd-practice.git"
            }
        }
        stage("Building the docker image"){
            steps{
                bat 'docker build -t ci-cd-practice .'
            }
        }
        stage("Running the tests"){
            steps{
                bat 'docker run --rm ci-cd-practice'
            }
        }
    }
}