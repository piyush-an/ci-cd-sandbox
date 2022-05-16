pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                // 
                echo "Building application ... "
            }
        }
        stage('Test') { 
            steps {
                // 
                echo "Testing application ... "
            }
        }
        stage('Deploy') { 
            steps {
                echo "Deploying application ... "
//                 withCredentials([ // Plugin Credentials and Credentials Bindings
//                     usernamePassword(credentials: 'login', usernameVariable: USER, passwordVariable: PWD)
//                 ]) {
//                     // sh "/path/scripts/some_script.sh ${USER} ${PWD} "
//                     echo  "/path/scripts/some_script.sh ${USER} ${PWD} "
//                 }
            }
        }
    }
}
