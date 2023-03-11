//with-parameter just select which parameter we are using

pipeline {
    agent any
    parameters {
        string(name: 'NAME', description: 'Please tell me your name?')
 
        string(job details: 'JOB_DETAILS' description: 'Please tell me your current job profile')
 
        booleanParam(name: 'SKIP_TEST', description: 'Want to skip running Test cases?')
 
        choice(name: 'BRANCH', choices: ['Master', 'Dev', 'qa', 'test'], description: 'Choose branch')
 
        password(name: 'SONAR_SERVER_PWD', description: 'Enter SONAR password')
    }
    stages {
        stage('Printing Parameters') {
            steps {
                echo "Hello ${params.NAME}"
 
                echo "Job Details: ${params.JOB_DETAILS}"
 
                echo "Skip Running Test case ?: ${params.SKIP_TEST}"
 
                echo "Branch Choice: ${params.BRANCH}"
 
                echo "SONAR Password: ${params.SONAR_SERVER_PWD}"
            }
        }
    }
}
