# Purpose
Microsoft removed NodeJS from their .NET Core Docker images ([announcement](https://github.com/aspnet/Announcements/issues/298)). This image adds back NodeJS for build time with Webpack pre-installed.

# Ingredients
* Based on docker image [mcr.microsoft.com/dotnet/sdk](https://hub.docker.com/_/microsoft-dotnet-sdk/):8.0.101-alpine3.18
* [NodeJS](https://nodejs.org/) 20.11.0
* [Gulp-cli](https://www.npmjs.com/package/gulp-cli) 2.3.0

# Full Tag Listing
## Linux amd64 tags
- [`6.0.418-bullseye-slim`, `6.0-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/6.0/sdk/bullseye-slim/gulp/Dockerfile)
- [`6.0.418-alpine`, `6.0-sdk-alpine` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/6.0/sdk/alpine/gulp/Dockerfile)
- [`7.0.405-bullseye-slim`, `7.0-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/7.0/sdk/bullseye-slim/gulp/Dockerfile)
- [`8.0.101-bookworm-slim`, `8.0-sdk`, `latest` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/8.0/sdk/bookworm-slim/gulp/Dockerfile)
- [`8.0.101-alpine`, `8.0-sdk-alpine` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/8.0/sdk/alpine/gulp/Dockerfile)
