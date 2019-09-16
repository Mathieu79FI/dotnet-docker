# Purpose
Microsoft removed NodeJS from their .NET Core Docker images ([announcement](https://github.com/aspnet/Announcements/issues/298)). This image adds back NodeJS for build time with Gulp pre-installed.

# Ingredients
* Based on docker image [mcr.microsoft.com/dotnet/core/sdk](https://hub.docker.com/_/microsoft-dotnet-core-sdk/):3.0.100-preview9
* [NodeJS](https://nodejs.org/) LTS 10.16.3
* [Gulp-cli](https://www.npmjs.com/package/gulp-cli) 2.2.0

# Full Tag Listing
## Linux amd64 tags
- [`2.2.402-sdk-stretch`, `2.2-sdk`, `latest` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/2.2/sdk/stretch/amd64/Dockerfile-gulp)
- [`3.0.100-preview9`, `3.0-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/3.0/sdk/stretch/amd64/gulp/Dockerfile)