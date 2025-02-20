# Purpose
Microsoft removed NodeJS from their .NET Core Docker images ([announcement](https://github.com/aspnet/Announcements/issues/298)). This image adds back NodeJS for build time with Gulp pre-installed.

# Ingredients
* Based on docker image [mcr.microsoft.com/dotnet/sdk](https://hub.docker.com/_/microsoft-dotnet-sdk/):6.0.428-1-bullseye-slim
* [NodeJS](https://nodejs.org/) 22.12.0
* [Gulp](https://www.npmjs.com/package/gulp) 5.0.0
* [Gulp-cli](https://www.npmjs.com/package/gulp-cli) 3.0.0
* [TypeScript](https://www.npmjs.com/package/typescript) 5.7.2

# Full Tag Listing
## Linux amd64 tags
- [`6.0.428-bullseye-slim`, `6.0-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/6.0/sdk/bullseye-slim/gulp/Dockerfile)
- [`6.0.428-alpine`, `6.0-sdk-alpine` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/6.0/sdk/alpine/gulp/Dockerfile)
