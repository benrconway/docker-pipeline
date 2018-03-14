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
         sh "docker container ls"
         sh 'docker image ls'
         sh 'docker rmi -f 564bab2b17fd'
         sh 'docker rmi -f 035dd96e862e'
         sh 'docker rmi -f 77312669f8e4'
         sh 'docker rmi -f eeffa9ca3a24'
         sh 'docker rmi -f ce4d5a5ade21'
         sh 'docker rmi -f 21752e500de2'
         sh 'docker rmi -f 913edbe005d7'
         sh 'docker rmi -f d350bea24299'
         sh 'docker rmi -f af7d0d169d90'
         sh 'docker rmi -f 918deefbd1da'
         sh 'docker rmi -f 2f40dd2656c9'
         sh 'docker rmi -f c0ff24884469'
         sh 'docker rmi -f c8bcfb0e0062'
         sh 'docker rmi -f 3c0f1a7fad93'
         sh 'docker rmi -f a63d09c3c046'
         sh 'docker rmi -f a7a3941dc500'
         sh 'docker rmi -f fb8ce4a6bcbe'
         sh 'docker rmi -f 8c71408489f7'
         sh 'docker rmi -f 2130039795c4'
         sh 'docker rmi -f 6cd32cc28ca0'
         sh 'docker rmi -f d9f0c8652756'
         sh 'docker rmi -f 397e39f152c0'
         sh 'docker rmi -f 4183edd02ecf'
         sh 'docker rmi -f 5d5aa44b999f'
         sh 'docker rmi -f 4e35516342a7'


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
