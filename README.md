### Publish Docker Image to AWS Elastic Container Registry

##### In here, the following workflow can use to publish the docker image to AWS Elastic Container Registry(ECR) using GitHub Action. This GitHub action will be triggered every time a new Git tag is pushed to the GitHub repository.


#### Create Environment Variables

1.Create <b>AWS ACCESS KEY</b> & <b>AWS SECRET ACCESS KEY</b> in your AWS account.

2.Go to your GitHub repositorie's <a href="https://github.com/{your_username}/{your_repository_name}/settings/secrets/actions">Settings => Secrets => Actions</a> and create two New Repsitory Secret. Name it <b>AWS_ACCESS_KEY_ID</b> and set the value to your created <b>AWS ACCESS KEY</b> & <b>AWS_SECRET_ACCESS_KEY</b> and set the value to your created  <b>AWS SECRET ACCESS KEY</b>.

#### Publish new Docker Image with version number

As usual, stage your changes and then commit them. Then, run the folowing commands:

```
git tag <your_tag> 
```

Then run the following command to push changes to GitHub repository:

```
git push origin <tag_name>
```

The following workflow is designed to be triggered when a new Git tag is pushed project repository. Using the workflow, you can perform pushes to the repository (git push) without triggering this workflow. For example, when updating the project’s README file, you can run the following command:

```
git push <branch_name>
```



