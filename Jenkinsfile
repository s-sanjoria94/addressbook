pipeline {
    agent {label 'linux'} 

    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
    //        post {
    //            always {
    //                sh 'Archiving artifacts'
    //                archiveArtifacts artifacts: 'target/*.war', followSymlinks: false, onlyIfSuccessful: true
    //            }
    //        }
        }
        // stage('Deliver') {
        //     steps {
        //         sh './jenkins/scripts/deliver.sh'
        //     }
        // }
    }
}
