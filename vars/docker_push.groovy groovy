def call(String imageName, String imageTag, String dockerHubUser) {
    withCredentials([usernamePassword(
        credentialsId: 'dockerhub',
        usernameVariable: 'DOCKER_USER',
        passwordVariable: 'DOCKER_PASS'
    )]) {
        sh "docker login -u ${DOCKER_USER} -p ${DOCKER_PASS}"
        sh "docker push ${dockerHubUser}/${imageName}:${imageTag}"
    }
}
