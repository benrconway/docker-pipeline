node {

    def app

    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */
        // app = docker.build("api")
        sh 'docker build -t api .'

        // docker.build("api")
    }

    stage('Test image') {
        /* Ideally, we would run a test framework against our image.
         * For this example, we're using a Volkswagen-type approach ;-) */
         sh 'docker build -t api .'

         sh "docker run -p 3000:3000 api"
         sh "docker system prune"
         sh "docker container ls"
         sh 'docker image ls'
         //
         // docker.run("api")
         // docker.logs("api")
         //

        // app.run()
        // $echo '' < app.container("logs")
        // trying to see what it written instead of just receiving success  notification
        // app.inside{
        //   sh 'npm test'
        //}
    }
}
