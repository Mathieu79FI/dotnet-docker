# Purpose
Microsoft removed NodeJS from their .NET Core Docker images ([announcement](https://github.com/aspnet/Announcements/issues/298)). This image adds back NodeJS for build time with Grunt pre-installed.

# Ingredients
* Based on docker image [mcr.microsoft.com/dotnet/sdk](https://hub.docker.com/_/microsoft-dotnet-sdk/):5.0.403-alpine3.14
* [NodeJS](https://nodejs.org/) LTS 16.13.0
* [Grunt-cli](https://www.npmjs.com/package/grunt-cli) 1.4.3

# Full Tag Listing
## Linux amd64 tags
- [`2.2.402-sdk-stretch`, `2.2-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/2.2/sdk/stretch/amd64/Dockerfile-grunt)
- [`3.0.103-sdk-buster`, `3.0-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/3.0/sdk/buster/amd64/grunt/Dockerfile)
- [`3.1.415-sdk-buster`, `3.1-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/3.1/sdk/buster/amd64/grunt/Dockerfile)
- [`5.0.403-buster-slim`, `5.0-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/5.0/sdk/buster-slim/grunt/Dockerfile)
- [`5.0.403-bullseye-slim` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/5.0/sdk/bullseye-slim/grunt/Dockerfile)
- [`5.0.403-alpine`, `5.0-sdk-alpine` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/5.0/sdk/alpine/grunt/Dockerfile)
