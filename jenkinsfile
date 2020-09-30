node {
    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'Docker_Id') {

        def customImage = docker.build("anjuraju/nodejs-docker":${env.BUILD_ID}")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
