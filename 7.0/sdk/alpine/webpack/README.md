# Purpose
Microsoft removed NodeJS from their .NET Core Docker images ([announcement](https://github.com/aspnet/Announcements/issues/298)). This image adds back NodeJS for build time with Webpack pre-installed.

# Ingredients
* Based on docker image [mcr.microsoft.com/dotnet/sdk](https://hub.docker.com/_/microsoft-dotnet-sdk/):7.0.407-alpine3.18
* [NodeJS](https://nodejs.org/) LTS 20.11.1
* [Webpack](https://www.npmjs.com/package/webpack) 5.90.3
* [Webpack-cli](https://www.npmjs.com/package/webpack-cli) 5.1.4

# Full Tag Listing
## Linux amd64 tags
- [`6.0.420-bullseye-slim`, `6.0-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/6.0/sdk/bullseye-slim/webpack/Dockerfile)
- [`6.0.420-alpine`, `6.0-sdk-alpine` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/6.0/sdk/alpine/webpack/Dockerfile)
- [`7.0.407-bullseye-slim`, `7.0-sdk` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/7.0/sdk/bullseye-slim/webpack/Dockerfile)
- [`7.0.407-alpine`, `7.0-sdk-alpine` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/7.0/sdk/alpine/webpack/Dockerfile)
