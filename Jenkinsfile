pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                // 
            }
        }
        stage('Test') { 
            steps {
                // 
            }
        }
        stage('Deploy') { 
            steps {
                echo ""
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
