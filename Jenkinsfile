#!/usr/bin/env groovy

pipeline {
  def app
    
    environment {
      CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
              docker('testDocker'){
              app = docker.build("api")
                }
              // nodejs('testJS') {
              //   sh "npm install"
              //   sh "npm start &"
              // }

            }
        }
        stage('Test') {
            steps {
                echo 'Testing.. and stuff'

                app.run()
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
