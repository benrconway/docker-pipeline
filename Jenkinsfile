#!/usr/bin/env groovy
node {
    def app

    environment{
      CI='true'
      DOCKER = tool("testDocker")
    }

    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */
         sh "${DOCKER} build -t api ."
        // app = {DOCKER}.build("api")
    }

    stage('Test image') {
        /* Ideally, we would run a test framework against our image.
         * For this example, we're using a Volkswagen-type approach ;-) */
         sh "${DOCKER} run api"
        // app.inside {
        //     sh 'npm start'
        // }
    }
}
