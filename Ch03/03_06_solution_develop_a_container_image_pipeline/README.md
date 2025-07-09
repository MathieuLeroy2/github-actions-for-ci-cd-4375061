# 03_06_solution_develop_a_container_image_pipeline

See the ./docker-image.yml file 
    ! mathieuleroy2  should be changed to the github username of the student. This username should be LOWERCASE (even if it contains upper case letters)

# BONUS!  USE THE IMAGE
Congrats on building the image.  Why not use it too!?

Follow these steps:
1. Confirm that `docker` is running on your local system.
    - [Installing Docker Desktop](https://www.docker.com/products/docker-desktop/)
3. Download the image that was built, using the `main` branch as a reference:

        docker pull ghcr.io/GITHUB_USERNAME/GITHUB_REPONAME:main

1. In a terminal, start a container with the `docker run` command, and connecting the local port `3000` to the container port `3000`:

        docker run -p 3000:3000 ghcr.io/GITHUB_USERNAME/GITHUB_REPONAME:main

1. In a browser, open the URL [localhost:3000/](http://localhost:3000/).
1. Follow the instructions to see the API in action!
