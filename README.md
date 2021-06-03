# App Build Pipeline
* A repository for application source code
* Every git-push to the repository initiates a Build Pipeline-run
* The build pipeline typically builds the app, test it, build docker images and perhaps run integration tests. If everything has succeeded, it also push the image to an image registry. The last task in the pipeline would be to git-clone the application configuration respository and updated the image reference to the newly built image.
* The result of this pipeline is that it either failed on a certain task, or that it succeeded. And if it succeeded on the mainline (not a feature-branch) you probably want to initiate a Deployment Pipeline, typically with a git-push to the application configuration repo.