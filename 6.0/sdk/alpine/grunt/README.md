# Purpose
Microsoft removed NodeJS from their .NET Core Docker images ([announcement](https://github.com/aspnet/Announcements/issues/298)). This image adds back NodeJS for build time with Grunt pre-installed.

# Ingredients
* Based on docker image [mcr.microsoft.com/dotnet/sdk](https://hub.docker.com/_/microsoft-dotnet-sdk/):6.0.400-alpine3.16
* [NodeJS](https://nodejs.org/) LTS 16.16.0
* [Grunt-cli](https://www.npmjs.com/package/grunt-cli) 1.4.3

# Full Tag Listing
## Linux amd64 tags
- [`5.0.408-buster-slim`, `5.0-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/5.0/sdk/buster-slim/grunt/Dockerfile)
- [`5.0.408-bullseye-slim` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/5.0/sdk/bullseye-slim/grunt/Dockerfile)
- [`5.0.408-alpine`, `5.0-sdk-alpine` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/5.0/sdk/alpine/grunt/Dockerfile)
- [`6.0.400-bullseye-slim`, `6.0-sdk`, `latest` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/6.0/sdk/bullseye-slim/grunt/Dockerfile)
- [`6.0.400-alpine`, `6.0-sdk-alpine` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/6.0/sdk/alpine/grunt/Dockerfile)
