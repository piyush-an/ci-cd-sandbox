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
