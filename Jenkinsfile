pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Create directory to store HTML and CSS files
                sh 'mkdir -p build'
                // Copy HTML and CSS files to build directory
                sh 'echo \'<!DOCTYPE html><html><head><title> Home </title><link rel="stylesheet" type="text/css" media="screen" href="main.css"/></head><div ><img src="logo.svg" alt="Deakin" width="200" height="210" >UI Designer Tasks</div><body><h1>SIT223-SIT753 - Professional Practice in IT</h1><h2> Unit details</h2><table style="width:100%"><tr><td>Year: </td><td>2023 unit information</td></tr><tr><td>Enrolment modes:</td><td>Trimester 1: Burwood (Melbourne), Geelong, Cloud (online)</td></tr><tr><td>Credit point(s):</td><td>1</td></tr><tr><td> Unit Chair:</td><td> Trimester 1: Azadeh Ghari Neiat</td></tr><tr><td> Scheduled Learning Activities:</td><td> 1 x 3 hour active class per week, weekly drop in support.</td></tr></table><h3> Content</h3><p> To be successful IT graduates need to understand the use of industry tools and practices, the ways these tools work and connect together, and the underlying professional, ethical, and teamwork knowledge and skills needed to put these into practice in a professional maner.</p><h3>Hurdle requirement</h3><p> To be eligible to obtain a pass in this unit, students must meet certain milestones as part of the portfolio.</p><a href="https://www.deakin.edu.au/students/enrolment-and-fees/fees"> > Current students</a></body></html>\' > build/Index.html'
                sh 'echo \'h1 {font-size: 40px;font-family: Arial}h2 {font-size: 25px;font-family: Arial}h3 {font-family: Arial}p {font-size: 14px;font-family: Arial}th, td {padding: 8px;text-align: left;border-bottom: 1px solid #ddd;font-family: Arial}tr:nth-child(odd) {background-color: #f2f2f2;}div { background-color: blue;text-align: right;}\' > build/main.css'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                // Task: Run unit tests
                // Task: Run integration tests
                // Tools: JUnit, TestNG, Selenium, Postman
                sh 'echo "Run unit tests"'
                sh 'echo "Run integration tests"'
            }
        }
        stage('Code Analysis') {
            steps {
                // Task: Integrate a code analysis tool to analyze the code
                // Tool: SonarQube, Checkstyle, PMD
                sh 'echo "Run code analysis"'
            }
        }
        stage('Security Scan') {
            steps {
                // Task: Perform a security scan on the code
                // Tool: OWASP ZAP, SonarQube, Snyk
                sh 'echo "Perform security scan"'
            }
        }
        stage('Deploy to Staging') {
            steps {
                // Task: Deploy the application to a staging server
                // Tool: Ansible, Docker, AWS CodeDeploy
                sh 'echo "Deploy to staging server"'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                // Task: Run integration tests on the staging environment
                // Tools: Selenium, Postman
                sh 'echo "Run integration tests on staging"'
            }
        }
        stage('Deploy to Production') {
            steps {
                // Task: Deploy the application to a production server
                // Tool: Ansible, Docker, AWS CodeDeploy
                sh 'echo "Deploy to production server"'
            }
        }
    }

    post {
        always {
            // Send email notifications at the end of test and security scan stages
            emailext subject: "Pipeline Status - ${currentBuild.result}",
                      body: "The pipeline has finished. Status: ${currentBuild.result}",
                      to: "tejasvarunbaskar@gmail.com",
                      attachLog: true
        }
    }
}
