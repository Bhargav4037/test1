# deployApp
deployApp is a CLI (Command Line Interface) application written in Go, designed to deploy the applications and detect the cloud components used in that applications.

## Table of contents

- Installation
- Building the application
- Running the application
- Running the unit tests

## Installation

To install the deployapp application you need to have the [go](https://go.dev/doc/install) and [gcloud](https://cloud.google.com/sdk/docs/install) installed on your machine .

## Building the application

To build the application, follow these steps:

1. Clone this repository:
   ```sh
   git clone https://config-management.googlesource.com/prototype
   ```

2. Navigate to the project directory:
   ```sh
   cd prototype/deployapp/
   ```

3. Build the application:
   ```sh
   go build -o deployApp
   ```

This will create an executable file named `deployApp` in your project directory. 

## Running the application

Before running the application make sure you have authenticated with the Application Default Credentials if not run the following command.
```sh
gcloud auth application-default login
```
A sign-in screen appears. After you sign in, your credentials are stored in the local credential file used by ADC.

To run the application, give the githubURL of the application that you need to deploy and detect the cloud components to the flag --githubURL ,also give the value to the boolean flag --useAI as shown below.
```sh
./deployapp --githubURL <Github URL> --useAI=<boolean value>
```
If useAI is true it prompts for the GCP project details first asks for the projectId by clicking enter it asks for the location of the Project like shown below.
```sh
Please enter your GCP project ID for calling the Vertex AI model (e.g., my-gcp-123) and press enter:

Please enter your GCP project location for calling the Vertex AI model (e.g., us-central1) and press enter:
```
It prompts you whether you need to build the application or not. By entering "yes", It generates the Dockerfile and cloudbuild.yaml file if the cloned application don't have them.
If they have them for each it ask whether you want to overwrite them or let it be. Based on your response "yes"/"no" to overwrite finally application will have cloudbuild.yaml and Dockerfile.
After this it builds the docker image and store it in the artifact registry this step may take more time wait for it.

## Running the unit tests

To run the unit tests for each functionality, follow these steps:

1. Navigate to functionality directory that you need to test from project directory, Example:
   ```sh
   cd clonerepo
   ```

2. Test the functionality directory by this command:
   ```sh
   go test
   ```

3. To take closer look on tests:
   ```sh
   go test -v
   ```

   




