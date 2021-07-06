# Better Serverless API (BeSA)
A framework for building better serverless api.

# Abstract

This is a proposal for a framework for building enterprise-grade serverless APIs. There are many libraries that try to ease the development of serverless API development but none of them can do it nicely. The main aim of this framework is to enable developers to write/debug/test APIs locally (the way APIs have been built for ages), and when ready with the single command it can produce all necessary infrastructure components in the cloud. INITIALLY, THIS IS AIMED AT AWS REST API DEVELOPMENT.

# The What
Framework for building serverless APIs, leveraging tools that are familiar to developers. The framework should attract away all config that is required to provision serverless infrastructure (one way is to leverage AWS CDK to do this with some pre-defined high-level constructs). 

# The Why
All the existing libraries for building serverless APIs, focus on optimizing the provisioning of resources and do not put any solutions forward for the actual CODE that will be running the business logic. In contrast, Frameworks such as Nestjs focus more on improving the API development experience and are where the developer will. be spending most of his time. The goal of this framework is to be like Nestjs (Declarative) but also take care of provisioning resources to run the API.

# How
For the PoC, we will start with extending Nestjs and leveraging the existing `Standalone applications` feature and will implement the logic for provisioning this individual controller. 

## Roadmap
- [ ]  Enable Nestjs like declaration based API development
- [ ]  Implement custom request validations using class-validator and AWS API gateway request validation models
- [ ] Configure AWS SAM to simulate development environment to run individual controllers as they would run in the cloud
- [ ] Ability to generate API docs based on built-in Open API generator
- [ ] Implement Custom Authorizers in a similar fashion to how Nestjs Guards work
- [ ] Explore the possibility for allowing consumption for other event sources (sns, sqs, etc, perhaps a different module?)
- [ ] Produce Benchmarks of running a serveless APIs in an express based lambda, or in individual components

