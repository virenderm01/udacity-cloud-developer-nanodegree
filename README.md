# udacity-cloud-developer-nanodegree
The repository is for people facing issues with the cloud developer nanodegree program to run the modules on windows 10 home OS

## Running the Monolith application locally
> Few issues I faced was with how the server.js is picked and packed.
Make sure that the *main* in package.json points to **www/server.js** instead of **src/server.js**


## Docker Module
> Passing volume for the docker.
> To pass the volume *-v* you should start with **//** and should not use **:** in the *docker run* command.

 `docker run --rm --publish 8080:8080 -v //c/Users/username/.aws://root/.aws --env POSTGRES_HOST=%POSTGRES_HOST% --env POSTGRES_USERNAME=%POSTGRES_USERNAME% --env POSTGRES_PASSWORD=%POSTGRES_PASSWORD% --env POSTGRES_DATABASE=%POSTGRES_DATABASE% --env AWS_REGION=%AWS_REGION% --env AWS_PROFILE=%AWS_PROFILE% --env AWS_BUCKET=%AWS_MEDIA_BUCKET% --env JWT_SECRET=%JWT_SECRET% --name feed username/udacity-restapi-feed`
 
 > This is assuming that your AWS credentials are stored in the _C drive_
 
 ## Creating kubernete cluster on AWS
 1. Create an EC2 instance in your AWS account.
 2. Login to the instance
 3. Install the kubeone from the documentation provided 
 ```
     * curl -LO https://github.com/kubermatic/kubeone/releases/download/v<version>/kubeone_<version>_<operating_system>_amd64.zip
     * unzip kubeone_<version>_<operating_system>_amd64.zip -d kubeone_<version>_<operating_system>_amd64
     * sudo mv kubeone_<version>_<operating_system>_amd64/kubeone /usr/local/bin
```
4. Install terraform 
```
    * curl -LO https://releases.hashicorp.com/terraform/<version>/terraform_<version>_linux_amd64.zip
    * unzip terraform_<version>_linux_amd64.zip -d terraform_<version>_linux_amd64
    * sudo mv terraform_<version>_linux_amd64/terraform /usr/local/bin
```
5. change directory to *kubeone_<version>_linux_amd64/examples/terraform/aws*
6. Run `terraform init`
7. You will now need to create the ssh keys and set the AWS key, secret and security token
