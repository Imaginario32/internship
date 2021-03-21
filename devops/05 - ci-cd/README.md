## Prerequsite

* Minikube v1.6.2 or greater

* Docker 19.03 or greater

* Git 2.28 or greater

## Questions

1. What is git flow and its variations?
  Git flow is a branching model of Git. Gitflow is ideal for projects where the release cycle is on schedule. Variations: GitHub Flow, Gitlab Flow

2. What is Continuous integration ?
  Continuous integration - is a practice software development, which is to perform frequent automatic assemblages project for the early detection and resolution of integration problems

3. What is Continuous deployment?
  Continuous deployment is a software release process that uses automated testing to validate if changes to a codebase are correct and stable for immediate autonomous deployment to a production environment

4. What types of deployment can you name and describe ? (Green-blue, etc.)
  - Blue green deployment involves have two instances of your application in separate servers. Where the green instance is the live/production instance and the blue instance is the new setup you intend switching too.
  - Canary deployment is used to release features in batches. This method of deployment allows for user feedback before general roll out to all infrastructure. In canary model, you have set of servers/infrastructure resources dedicated to a set of users
  - Atomic deployment - this deployment method involves using a single instance to perform deployment and changing directories when the new deployment is done. This type of deployment is used when there is limit to infrastructure you can use.

5. What types of testing do you know? What are they?
  Unit tests - consist in testing individual methods and functions of the classes, components or modules used by your software
  Integration tests - verify that different modules or services used by your application work well together.
  Functional tests - They only verify the output of an action and do not check the intermediate states of the system when performing that action.
  End-to-end tests - replicates a user behavior with the software in a complete application environment
  Acceptance testing - are formal tests executed to verify if a system satisfies its business requirements.
  Performance testing - check the behaviors of the system when it is under significant load.
  Smoke testing - are basic tests that check basic functionality of the application.
  Smoke tests can be useful right after a new build is made to decide whether or not you can run more expensive tests, or right after a deployment to make sure that they application is running properly in the newly deployed environment.
  

6. `*` Describe how the code from the developer's computer reaches the production environment? What stages would you set up?
  Development environment - Software repository - CI/CD environment -Testing - Staging environment - Deploy production


## Tasks

* Log in to https://circleci.com/ with your github account

* Edit `.circleci/config.yaml` and create pipelines that:
    * build your [dockerfile](../02%20-%20dockerfile/Dockerfile) with new version tag and store in into a registry (dockerhub or smth else with public access)

    *  `*` update your [docker-compose](../03%20-%20docker-compose/example/docker-compose.yaml) with a new tag and create new release with changelog

    *  `*` update you helm charts and umbrella helm chart, create release in your repository, download release and redeploy umbrella helm chart to minikube for testing
