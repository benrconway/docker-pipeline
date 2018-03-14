node {

    def app
    environment{
      DOCKER = tool('testDocker')
    }
    stage('Clone repository') {
        /* Let's make sure we have the repository cloned to our workspace */

        checkout scm
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */
        // app = docker.build("api")

        //This one works in my docker container jenkins.
        sh 'docker build -t api .'

        //Experiment to see if I can get docker on my personal machine working
        // sh "sh ${DOCKER}/Contents/Resources/bin/docker build -t api . "
    }

    stage('Test image') {
        /* Ideally, we would run a test framework against our image.
         * For this example, we're using a Volkswagen-type approach ;-) */
         // sh 'docker build -t api .'

         sh "docker run -p 3000:3000 api"


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
