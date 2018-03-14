node {

    def app

      // DOCKER = tool("testDocker")


    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */
        app = docker.build("api")
    }

    stage('Test image') {
        /* Ideally, we would run a test framework against our image.
         * For this example, we're using a Volkswagen-type approach ;-) */
        sh '$echo app.run()'
        // trying to see what it written instead of just receiving success  notification
        // app.inside{
        //   sh 'npm test'
        //}
    }
}
