# Purpose
Microsoft removed NodeJS from their .NET Core Docker images ([announcement](https://github.com/aspnet/Announcements/issues/298)). This image adds back NodeJS for build time with Grunt pre-installed.

# Ingredients
* Based on docker image [mcr.microsoft.com/dotnet/sdk](https://hub.docker.com/_/microsoft-dotnet-sdk/):6.0.424-bullseye-slim
* [NodeJS](https://nodejs.org/) LTS 20.15.1
* [Grunt](https://www.npmjs.com/package/grunt) 1.6.1
* [Grunt-cli](https://www.npmjs.com/package/grunt-cli) 1.4.3

# Full Tag Listing
## Linux amd64 tags
- [`6.0.424-bullseye-slim`, `6.0-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/6.0/sdk/bullseye-slim/grunt/Dockerfile)
- [`6.0.424-alpine`, `6.0-sdk-alpine` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/6.0/sdk/alpine/grunt/Dockerfile)
