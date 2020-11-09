# Continuous Delivery Using Docker and Ansible

## Course overview:
- Unit and integration tests using Docker
- Building and testing Docker release images
- Push-button style automation for continuous delivery and deployment
- Continuous delivery pipeling using Jenkins
- Set up a deployment pipeline that deploys your application to AWS

## Course Introduction

### Introduction
- Continuous Delivery: practice of creating repeatable reliable process for releasing software
  - release often
  - release faster
  - greater reliability
  - in business terms: is a key enabler for organisations that deliver applications and digital services, derives
  - business benefits: innovation, fast feedback, warranty (bugs are discovered early with less cost)
- course goal: continuous delivery workflow/pipeline with python, docker, jenkins, github, docker hub, ansible, AWS

### Course Audience and Prerequisites

- Developers:
    - wrap test and build actions in docker
    - you applications work on any machine
    - run production-like environment locally
    - fast track your changes to production

- Operations:
  - Build continuous Delivery pipelines
  - automate test, build, release and deploy
  - setup continuous delivery systems
  - infrastructure as code

- Architects:
  - application agnostic methodology
  - run on any CD system
  - immutable infrastructure
  - Infrastructure as Code

- Prerequisites:
  - Docker: basic understanding of Docker (course docker deep dive on pluralsight)
  - Ansible
  - application delivery

- Development environment:
  - mac os x
  - linux
  - windows + linux vm

### Course Tour
- create sample application: sample app, unit and integration tests, acceptance tests
- unit/integration testing: test stage, docker images, docker and docker compose building blocks
- building artifacts using docker: build stage, test stage consistency, creating built distributions
- creating releases using docker: release stage, release image, release environment
- continuous delivery automation: make build system, github repos, docker hub repos
- enhancing the workflow: production ready, error/failure handling, tag publish
- continuous delivery using jenkins: jenkins, github/docker hub integration, runnning jenkins in AWS
- continuous deployment using ansible: ansible deployment playbook, infrastructure as code, end-to-end continuous Delivery

### Continuous Delivery overview
#### Why?
- delivering business value as quickly and efficiently as possible
- release often
- release small
- minimum viable product
- test your ideas in the real world - fast feedback
- build better smarter products
- reduce risk, smaller changes and less risk
  - continuously deploy:
    - to at least one environment
    - always deploying means you get much better at deployments
  - small scope of change:
    - easier to deploy
    - easier to fix
- real progress:
  - each change is real progress
    - you know it's done because you deployed it successfully
  - build confidence
    - in ability to release new features
    - in ability to detect and fix issues

### How to achieve continuous delivery?
- methodology
  - application agnostic
  - portability
  - separation of concerns
  - and more: immutable infrastructure, infrastructure as code
- automation:
  - saves time and money
  - repeatable and consistent results
  - automate as much as possible
    - tests
    - creating environments
    - deployments
    - monitoring
    - etc.
- testing:
  - quantitative measurement
  - production readiness
  - automation and consistency
- people: everyone needs to be accountable and priority must always be on applications being up and running, without the right attitude and desire from people (developers and managers) it is difficult to maintain CD

### Why docker?
- speed
- portability: abstract and immutable runtime environment
- automation

### Continuous Delivery Architecture
#### Continuous Delivery Overflow
- test > build > release > deploy
- test: testing internals of the application
  - unit and integration testing
  - use docker to wrap test runners
    eg. maven, gradle (Java)
    eg. manage.py (Python Dango)
  - benefits of using Docker
    - predefined environment
    - portable, consistent, repeatable
- build:
  - build application artifacts
    - eg. Python Wheels
    - eg. Java JAR files
  - must represent as tested application state
  - creates a deployable artifact
    - i.e. a built distribution
    - pre-compiled, pre-built
    - installation requires no development dependencies
- release:
  - build docker release image
    - includes minimal runtime environment
    - installs application artifacts
  - release environment
    - a production-like environment
    - use an external test runner to run acceptance tests
  - tag and publish:
    - only if acceptances tests pass
    - docker hub
- deploy stage
  - deploy release image to
    - at least one environment
    - eg. Development environment
    - eg. QA or Staging environments
    - perhaps even production
  - fully automated deployments
    - using orchestration tools such as Ansible
    - leverage infrastructure automation tools such as AWS CloudFormation

### Demo

- choosing virtualization platform: VirtualBox(free), VMWare Fusion, Parallels

- installing brew: (already installed)
$ brew -v
$ brew update

- installing Docker tools: Docker, Docker Compose, Docker Machine -> Docker Toolbox
$ brew install docker-compose

- this has dependencies on both docker and docker-machine so will install everything you need
- you want to install separately or to make sure:
  - Docker:
    $ brew install docker
  - Docker-machine
  $ brew install docker-machine

- Installing Ansible
- prerequisite: latest version of Python 2.7
$ python -V #check version before installing
$ brew install python
$ pip install pip --upgrade
$ pip install ansible --upgrade
$ pip install boto boto3
$ pip install awscli

- Installing Other tools
$ brew install git
$ brew install tree
& docker hub

- Creating a Docker Virtual Machine
$ docker-machine create --driver=virtualbox docker01
$ docker-machine env docker01
$ eval $(docker-machine env docker01)
- Creating the Course Root Folder
