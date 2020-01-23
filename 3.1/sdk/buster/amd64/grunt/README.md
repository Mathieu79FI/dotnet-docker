# Purpose
Microsoft removed NodeJS from their .NET Core Docker images ([announcement](https://github.com/aspnet/Announcements/issues/298)). This image adds back NodeJS for build time with Grunt pre-installed.

# Ingredients
* Based on docker image [mcr.microsoft.com/dotnet/core/sdk](https://hub.docker.com/_/microsoft-dotnet-core-sdk/):3.1.101-buster
* [NodeJS](https://nodejs.org/) LTS 12.14.1
* [Grunt-cli](https://www.npmjs.com/package/grunt-cli) 1.3.2

# Full Tag Listing
## Linux amd64 tags
- [`2.2.402-sdk-stretch`, `2.2-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/2.2/sdk/stretch/amd64/Dockerfile-gulp)
- [`3.0.102-sdk-buster`, `3.0-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/3.0/sdk/buster/amd64/grunt/Dockerfile)
- [`3.1.101-sdk-buster`, `3.1-sdk`, `latest` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/3.1/sdk/buster/amd64/grunt/Dockerfile)
