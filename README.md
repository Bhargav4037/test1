# deployapp
deployapp is a CLI (Command Line Interface) application written in Go, designed to deploy the applications and detect the cloud components used in that applications.

## Table of contents

- Installation
- Building the application
- Running the application
- Running the unit tests

## Installation

To install the deployapp application you need to have the [go](https://go.dev/doc/install) installed on your machine.

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
   go build -o deployapp
   ```

This will create an executable file named `deployapp` in your project directory. 

## Running the application

To run the application, give the githubURL of the application that you need to deploy and detect the cloud components to the flag --githubURL ,also give the value to the boolean flag --useAI as shown below.
```sh
./deployapp --githubURL <Github URL> --useAI=<boolean value>
```

## Running the unit tests

To run the unit tests for each functionality, follow these steps:

1. Navigate to clonerepo directory from project directory:
   ```sh
   cd clonerepo
   ```

2. Test the clone repo functionality:
   ```sh
   go test
   ```

3. To take closer look on tests:
   ```sh
   go test -v
   ```

   




