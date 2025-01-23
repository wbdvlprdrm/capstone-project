# CAPSTONE PROJECT

### Dockerfile Creation in the Google Cloud Shell

The first process it was download the github repository using the command and all the steps from this website and using the GLI from Google> https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository and downloading the repository that was given:  https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository.

After that, the next step was the creation of a Dockerfile, using command nano and then, the creation of the image and the container. 

Finally, it used the command curl http://localhost:8080 to pull up the website locally.


### Push the image to Artifact registry
During this process, the first step was to enable the API options to Deploy API, Build API, Cloud storage and Cloud Run Admin API. To find this option, we looked it up through the search bar in the GCP. 

Then, to create the image within Artifact registry, we created the repository with GCP and it was used the terminal to add it there using the commands:
> docker build -f Dockerfile docker tag webserver:latest LOCATION docker.pkg.dev/ramiro-h/repo-created/webserver:latest
>gcloud auth configure-docker LOCATION-docker.pkg.dev
>docker push us-west1-docker.pkg.dev/ramoroh/quickstart-docker-repo/webserver:latest
>us-west1-docker.pkg.dev/ramiroh/quickstart-docker-repo/webserver

Finally, the image was created and then, next to the image, we can see an option button where we can select the options to Deploy Cloud Run, Deploy GCE and Deploy GKE.

### Deployment in Cloud Run
To deploy the image in Cloud Run(GCP) we can follow the next steps:
After to build the Docker image, and push the image to registry, we opened the Cloud run deploy UI, and we create and select the service name. Choose the region or the container where it was the image, added the authentication settings and Click on Deploy.
Deployment in GCE
We created the VM instance and added the details and permissions from the network, and we clicked on the option to deploy on GCE from the artifact registry image and  finally provided us the external IP and clicked on the link and redirected us to the website.

### Deployment in GKE
We click on Deploy GKE from the artifact registry image and redirect us to the GKE option to create a Cluster and add the details from the new cluster. We filled the options and took a few minutes to do the deployment but finally provided us with the external IP and clicked on the link and redirected us to the website. The documentation that we followed> https://cloud.google.com/artifact-registry/docs/integrate-gke

### Deployment in App Engine
We looked at the documentation of how to do a deployment in App Engine and we found this> https://cloud.google.com/artifact-registry/docs/integrate-app-engine.
Then, we followed the instructions and we worked on the Cloud shell terminal, we got the link to view the app. 

### Upload the repository to GitHub
As a final step, we had to upload the repository to Github using the Terminal and command line. We found value information with these links: >https://docs.github.com/en/migrations/importing-source-code/using-the-command-line-to-import-source-code/adding-locally-hosted-code-to-github
>https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-authentication-to-github#authenticating-with-the-command-line

Following the steps, we could upload everything to Github

