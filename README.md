# App Build Pipeline
* A repository for application source code.
* Every git-push to the main branch of the repository initiates a pipeline run.
* The build pipeline builds adn publishes the app Docker image and tests it. If everything has succeeded, it updates the release id variable in the Azure DevOps Pipeline Library (variable groups).
* The release pipeline is triggered by succesfully finishing the Release stage of the build pipeline.