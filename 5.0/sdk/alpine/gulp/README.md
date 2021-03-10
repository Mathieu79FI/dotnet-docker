# Purpose
Microsoft removed NodeJS from their .NET Core Docker images ([announcement](https://github.com/aspnet/Announcements/issues/298)). This image adds back NodeJS for build time with Gulp pre-installed.

# Ingredients
* Based on docker image [mcr.microsoft.com/dotnet/sdk](https://hub.docker.com/_/microsoft-dotnet-sdk/):5.0.103-alpine3.13
* [NodeJS](https://nodejs.org/) LTS 14.16.0
* [Gulp-cli](https://www.npmjs.com/package/gulp-cli) 2.3.0

# Full Tag Listing
## Linux amd64 tags
- [`2.2.402-sdk-stretch`, `2.2-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/2.2/sdk/stretch/amd64/Dockerfile-gulp)
- [`3.0.103-sdk-buster`, `3.0-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/3.0/sdk/buster/amd64/gulp/Dockerfile)
- [`3.1.406-sdk-buster`, `3.1-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/3.1/sdk/buster/amd64/gulp/Dockerfile)
- [`5.0.201-buster-slim`, `5.0-sdk`, `latest` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/5.0/sdk/buster-slim/gulp/Dockerfile)
- [`5.0.201-alpine`, `5.0-sdk-alpine` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/5.0/sdk/alpine/gulp/Dockerfile)
