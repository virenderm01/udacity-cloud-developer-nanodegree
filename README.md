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
 
 
