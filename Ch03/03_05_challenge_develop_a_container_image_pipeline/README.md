# 03_05_challenge_develop_a_container_image_pipeline
It's time for a challenge!

You’ve just joined a team that’s developing an API for mobile applications.  They’re using containers for the first time and need to set up a CI/CD pipeline to publish container images.

The team has asked you to help them set up a repo for automatic docker deployment so it can be used in the latest project and any new projects that come up in the future.

# REQUIREMENTS
1. Create a new public repo.
2. In the repo, add the exercise files and then create a workflow using the starter workflow for *Publish Docker Container*.

    Additionally, add permissions for the integration workflow.  After the `uses` block, add:

        permissions:
          contents: read
          packages: write

3. Add a step to login to Github Container registry
         - name: Log in to GitHub Container Registry
            run: echo "${{ secrets.GITHUB_TOKEN }}" | docker login ghcr.io -u ${{ github.actor }} --password-stdin

5. Add a step to push the docker image to GHCR
         - name: Push Docker image to GHCR
            run: |
            docker push ghcr.io/mathieuleroy2/cicd:latest


Try running your automatically created image locally
