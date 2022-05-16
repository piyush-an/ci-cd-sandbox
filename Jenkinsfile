pipeline {
    agent any
    tools{
        // gradel, maven and jdk
        maven Maven
    }
    parameter{
        string(name: 'VERSION', defaultValue: '', description: 'version to deploy in prod')
        choice(name: 'VERSION', choices: ['1.0','1.1','1.2'], description: '')
        booleanParm(name: 'executeTest', defaultValue: true, description: '')
    }
    }
    environment {
        // Global : BRANCH_NAME , CHANGE_ID , CHANGE_URL , BUILD_NUMBER , BUILD_ID , 
        //          JOB_NAME , JOB_BASE_NAME , JENKINS_HOME , JENKINS_URL , BUILD_URL , JOB_URL
        //          GIT_BRANCH , GIT_LOCAL_BRANCH , GIT_URL

        NEW_VERSION = '1.3.0' // local variables 
        // SERVER_CREDENTIALS = credentials('credential_name')
    }
    stages {
        stage('Build') { 
            steps {
                echo "building the application .."
                echo "building version: ${NEW_VERSION}"

            }
        }
        stage('Test') {
            when {
                expression{
                    params.executeTest
                }
            }
            steps {
                echo "testing the application"
            }
        }
        stage('Deploy') { 
            steps {
                echo "deploying the application"
                // echo "deploying with ${SERVER_CREDENTIALS}"
                // sh /script/deploy.sh ${SERVER_CREDENTIALS}
                withCredentials([ // Plugin Credentials and Credentials Bindings
                    usernamePassword(credentials: 'credential_name', usernameVariable: USER, passwordVariable: PWD)
                ]) {
                    // sh "/path/scripts/some_script.sh ${USER} ${PWD} "
                    echo  "/path/scripts/some_script.sh ${USER} ${PWD} "
                }



            }
        }
    }
}
