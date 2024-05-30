# deployapp
deployapp is a CLI (Command Line Interface) application written in Go, designed to deploy the applications and detect the cloud components used in that applications.

## Table of contents

- [Installation] (https://github.com/Bhargav4037/test1/README.md#installation)
- [Building the application] (#building-the-application)
- [Running the application] (#running-the-application)
- [Running the unit tests] (#run-the-unit-tests)

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

To run the application, give the githubURL to the flag --githubURL as shown below, of the application that you need to deploy and detect the cloud components used in it.
```sh
./deployapp --githubURL <Github URL>
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

   




