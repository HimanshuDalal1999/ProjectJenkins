pipeline {
    agent any

    stages {
        stage('Get the code from GitHub') {
            steps {
                git 'https://github.com/HimanshuDalal1999/JenkinsProject'
            }
        }
        stage('Execution of Maven project on FireFox Browser') {
            steps {
                bat "mvn -Dmaven.test.failure.ignore=true clean test -Dclibrowser=firefox"
            }
            post {
            always {

            emailext attachLog: true, attachmentsPattern: 'target/cucumber-reports/reports.html', body: '''Hey Team,
<p>Here is the details of Execution through Jenkins<br>

$PROJECT_NAME - Build # $BUILD_NUMBER - $BUILD_STATUS:<br>

Check console output at $BUILD_URL to view the results.<br>

Thanks,<br>
Automation Team - ATT 19-August <h3>(Himanshu)</h3>''', subject: '$PROJECT_NAME - Build # $BUILD_NUMBER - $BUILD_STATUS! - Execution of Maven project on Mozila FireFox Browser', to: 'himanshudalal76247@gmail.com'
        }
    }
        }

        stage('Execution of Maven project on Microsoft Edge Browser') {
            steps {
                bat "mvn -Dmaven.test.failure.ignore=true clean test -Dclibrowser=Edge"
            }
            post {
            always {

            emailext attachLog: true, attachmentsPattern: 'target/cucumber-reports/reports.html', body: '''Hey Team,
<p>Here is the details of Execution through Jenkins<br>

$PROJECT_NAME - Build # $BUILD_NUMBER - $BUILD_STATUS:<br>

Check console output at $BUILD_URL to view the results.<br>

Thanks,<br>
Automation Team - ATT 19-August <h3>(Himanshu)</h3>''', subject: '$PROJECT_NAME - Build # $BUILD_NUMBER - $BUILD_STATUS! - Execution of Maven project on Microsoft Edge Browser', to: 'himanshudalal76247@gmail.com'
        }
    }
        }
        

     stage('Execution of Maven project on Google Chrome Browser') {
            steps {
                bat "mvn -Dmaven.test.failure.ignore=true clean test -Dclibrowser=chrome"
            }
            post {
            always {

            emailext attachLog: true, attachmentsPattern: 'target/cucumber-reports/reports.html', body: '''Hey Team,
<p>Here is the details of Execution through Jenkins<br>

$PROJECT_NAME - Build # $BUILD_NUMBER - $BUILD_STATUS:<br>

Check console output at $BUILD_URL to view the results.<br>

Thanks,<br>
Automation Team - ATT 19-August <h3>(Himanshu)</h3>''', subject: '$PROJECT_NAME - Build # $BUILD_NUMBER - $BUILD_STATUS! - Execution of Maven project on Google Chrome Browser', to: 'himanshudalal76247@gmail.com'
        }
    }
        

     }
        
  }

}
