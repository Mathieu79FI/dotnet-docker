# Purpose
Microsoft removed NodeJS from their .NET Core Docker images ([announcement](https://github.com/aspnet/Announcements/issues/298)). This image adds back NodeJS for build time with Webpack pre-installed.

# Ingredients
* Based on docker image [mcr.microsoft.com/dotnet/sdk](https://hub.docker.com/_/microsoft-dotnet-sdk/):5.0.403-bullseye-slim
* [NodeJS](https://nodejs.org/) LTS 16.13.0
* [Webpack](https://www.npmjs.com/package/webpack) 5.62.1
* [Webpack-cli](https://www.npmjs.com/package/webpack-cli) 4.9.1

# Full Tag Listing
## Linux amd64 tags
- [`5.0.403-buster-slim`, `5.0-sdk`, `latest` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/5.0/sdk/buster-slim/webpack/Dockerfile)
- [`5.0.403-bullseye-slim` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/5.0/sdk/bullseye-slim/webpack/Dockerfile)
- [`5.0.403-alpine`, `5.0-sdk-alpine` (*Dockerfile*)](https://github.com/Mathieu79FI/dotnet-docker/blob/master/5.0/sdk/alpine/webpack/Dockerfile)
