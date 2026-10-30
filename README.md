# CI/CD Tools and Practices Final Project

**Project name:** `ci-cd-final-project`

This repository contains my Final Project for the Coursera course **CI/CD Tools and Practices**. It is a Python Flask hit-counter microservice with a complete CI/CD pipeline:

- **Continuous Integration (GitHub Actions):** `.github/workflows/workflow.yml` lints the code with **flake8** and runs the unit tests with **nose** on every push and pull request to `main`.
- **Continuous Delivery (Tekton on OpenShift):** `.tekton/tasks.yml` defines the `cleanup` and `nose` tasks; `.tekton/pipeline.yml` runs cleanup, git-clone, flake8, nose, buildah and deploy (openshift-client) to build the image and deploy the service to OpenShift on port 8000.

## Project details

| Item | Value |
|---|---|
| Project name | ci-cd-final-project |
| Course | CI/CD Tools and Practices (IBM, Coursera) |
| Application | Hit Counter Service (Python 3.9, Flask, gunicorn) |
| Service port | 8000 |
| CI | GitHub Actions: flake8 lint, nose unit tests |
| CD | Tekton / OpenShift Pipelines |

## Setup

After entering the lab environment you will need to run the `setup.sh` script in the `./bin` folder to install the prerequisite software.

```bash
bash bin/setup.sh
```

Then you must exit the shell and start a new one for the Python virtual environment to be activated.

```bash
exit
```

## License

Licensed under the Apache License. See [LICENSE](/LICENSE)

## Author

Kabir Raval ([Kabramba](https://github.com/Kabramba)), based on the template by Skills Network

## <h3 align="center"> © IBM Corporation 2023. All rights reserved. <h3/>
