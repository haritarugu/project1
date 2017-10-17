#deploy examples
Demonstrates various deployment scenarios to an Axon.ivy Engine.

- [single-project](single-project) shows how to deploy a single ivy project to the engine.
- [application](application) shows how a full ivy application (based on multiple sub-projects) can be built and deployed to the engine.

## Prerequisites
Before each deployment the defined application must already exist on the engine and the engine must run.

## separating production and staging
We recommend to work with maven profiles:
- As default: Deploy to a Axon.ivy engine, which is just used for development. In the example `env-dev` is the default profile.
- To deploy to a productive engine configure a non-default profile. In the example `env-prd` is a profile like that.

To run a maven build with a specific profile you must add `-P[profile_name]` as command line argument: `mvn clean deploy -Penv-prd`