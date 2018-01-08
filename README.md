# Liquid Citizen : Context API

This repository hosts the Liquid Citizen Context API, a building block of the Liquid Citizen project.

Right now, it is just populated with the auth0 example express app for authorization over RS256 and a docker setup consisting two containers, one hosting the node/express app and one hosting a default mongodb installation, whose data is persisted in the ./data folder.

## Endpoints

The sample includes these endpoints:

**GET** /api/public
* An unprotected endpoint which returns a message on success. Does not require a valid JWT access token.

**GET** /api/private
* A protected endpoint which returns a message on success. Requires a valid JWT access token with a `scope` of `read:messages`.

## Running the Sample With Docker

In order to run the example with docker you need to have `docker` installed, then just run `docker-compose up`.
