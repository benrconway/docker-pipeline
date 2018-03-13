#!/usr/bin/env groovy

pipeline {

  //
  // "def app"  causes issue with configuration.
    agent {
      dockerfile true
    }
    environment {
      CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
              docker('testDocker'){
                sh 'docker build -t api .'
                }

// Things not yet working for me
                 // docker.build("api")
              // nodejs('testJS') {
              //   sh "npm install"
              //   sh "npm start &"
              // }

            }
        }
        stage('Test') {
            steps {
                echo 'Testing.. and stuff'

                // app.run()
                // nodejs('testJS') {
                //     sh "npm test"
                // }


            }
        }
        // stage('Deploy') {
        //     steps {
        //         echo 'Deploying....'
        //     }
        // }
    }
}

// how does this change things
// pipeline {
//     agent any
//     stages {
//         stage('Build') {
//             steps {
//                 echo "building..."
//             }
//         }
//         stage('Test'){
//             steps {
//                 sh ''
//                 junit 'reports/**/*.xml'
//             }
//         }
//         stage('Deploy') {
//             steps {
//                 sh 'make publish'
//             }
//         }
//     }
// }
